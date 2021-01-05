# Workcalendar
**WORK in PROGRESS**

### DONE:
- **Europe:**
- Austria
- Belarus
- Belgium
- Bulgaria
- Croatia
- Cyprus
- Czech Republic
- Denmark
- Estonia
- Finland
- France
- Germany
- Greece
- Hungary
- Iceland
- Ireland
- Italy
- Latvia
- Lithuania
- Luxembourg
- Malta
- Monaco
- Netherlands
- Norway
- Poland
- Portugal
- Romania
- Russia
- Serbia
- Slovakia
- Slovenia
- Spain
- Sweden
- Ukraine

## Overview

Workcalendar is a go library that is supposed to handle holidays.


## Usage

```go
package main

import (
    "fmt"
	"time"

	"github.com/Gasoid/workalendar/europe/russia"
)

func main() {
    now := time.Now()
    // check whether a day is holiday
    if russia.IsHoliday(now) {
        h, _ := russia.GetHoliday(now)
        fmt.Printf("Holiday is %s", h)
    } else {
        fmt.Print("No holiday today")
    }

    // get holiday name
    march8 := time.Date(2020, time.March, 8, 0, 0, 0, 0, time.UTC)
    h, err := russia.GetHoliday(march8)
    if err != nil {
        fmt.Print("Hm, it is weird")
    } else {
        fmt.Printf("Holiday is %s", h)
    }
}

```
