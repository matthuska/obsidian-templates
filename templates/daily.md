start_time::
end_time::
status::
## TODOs
### Due this week
```dataview
TASK
FROM -#waiting
WHERE !completed AND due AND date(due).weekyear <= date("{{date:YYYY-MM-DD}}").weekyear AND date(due).year <= date("{{date:YYYY-MM-DD}}").year
SORT due
```
### Due this week (waiting)
```dataview
TASK
WHERE !completed AND due AND date(due).weekyear <= date("2023-11-27").weekyear AND date(due).year <= date("{{date:YYYY-MM-DD}}").year AND contains(text, "#waiting")
```
### All other open TODOs with no due date
```dataview
TASK
WHERE !completed AND !due
```
### Completed today
```dataview
TASK
WHERE completion = date("{{date:YYYY-MM-DD}}")
```
## Log


