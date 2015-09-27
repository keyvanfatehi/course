# course

command line tool to help me stay organized with my courses

all it does currently is scan current directory and up and up until it files a `course.json` file, then prints it out in a clean way

i currently just use it for it to print for me the course URL from whichever directory I am at, so I can quickly get to the course website by doing a cmd-click at my terminal

# example course.json

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
