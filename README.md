# course

command line tool to help me stay organized with my courses

all it does currently is scan current directory and up and up until it files a `course.json` file, then prints it out in a clean way

i currently just use it for it to print for me the course URL from whichever directory I am at, so I can quickly get to the course website by doing a cmd-click at my terminal

## example course.json

```json
{
  "url": "http://www.ics.uci.edu/~emilyo/teaching/info43f2015/",
  "department": "IN4MATX",
  "number": "43",
  "title": "INTRO TO SOFTWARE ENGINEERING",
  "lecture": {
    "code": "37000",
    "building": "BS3",
    "room": "1200",
    "meetings": [{
      "day": "tuesday",
      "start": "5:00 PM",
      "end": "6:20 PM"
    },{
      "day": "thursday",
      "start": "5:00 PM",
      "end": "6:20 PM"
    }]
  },
  "discussion": {
    "code": "37005",
    "building": "ET",
    "room": "202",
    "meetings": [{
      "day": "wednesday",
      "start": "1:00 PM",
      "end": "1:50 PM"
    }]
  }
}
```

## Mirroring

It seems college professors post lectures to their websites often, so I have added a mirroring capability that leverages wget under the hood.

`course mirror` will do the trick for most of these professors' websites.

Others need you to make use of the wget --accept-regex or --reject-regex. The course.json file accomodates this. For example to only accept links to powerpoint files and ignore all other links during the mirror process, you can add this to your course.json:

```
"mirror": {
  "accept": ".pptx"
},
```
