[![npm version](https://badge.fury.io/js/week-hours-picker.svg)](https://badge.fury.io/js/week-hours-picker)
[![Downloads](http://img.shields.io/npm/dm/week-hours-picker.svg?style=flat)](https://npmjs.org/package/week-hours-picker)

![](https://raw.githubusercontent.com/clobucks/week-hours-picker/master/preview.png)

# [week-hours-picker](https://clobucks.github.io/week-hours-picker)

Hours picker by week day

## Usage

- set `data-name` attr for getting value with form submiting

### UMD Module
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
</head>
<body>
    <div id="input" data-name="form-name"></div>

    <script src="https://unpkg.com/week-hours-picker@latest/src/index.js"></script>
    <script>
        (() => {    
            // initialState { [row]: [hours] }
            const state = {
                0: [1, 2, 5, 10],
                5: [4, 9, 10, 20],
            }
            
            // change callback
            function handleStateChange(newState) {
                console.log(newState)
            }

            const options = {

                // custom days names (it's default values)
                days: {
                    0: 'Monday',
                    1: 'Tuesday',
                    2: 'Wednesday',
                    3: 'Thursday',
                    4: 'Friday',
                    5: 'Saturday',
                    6: 'Sunday',
                },
                
                // custom class names for dom elements (it's default values)
                classes: {
                    active: '',
                    aside: '',
                    body: '',
                    container: '',
                    day: '',
                    grid: '',
                    header: '',
                    headerHour: '',
                    hour: '',
                    input: '',
                    node: '',
                    row: '',
                },
            }

            weekHoursPicker(
                document.querySelector('#input'), // required
                state, // optional
                handleStateChange, // optional
                options, // optional
            )
        })()
    </script>
</body>
</html>
```

### ESM Module

```javascript
import weekHoursPicker from 'week-hours-picker'

weekHoursPicker(
    document.querySelector('#input'), // required
    state, // optional
    handleStateChange, // optional
    options, // optional
)
```
