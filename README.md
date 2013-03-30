TimeRange
=========

Compare and loop time ranges in PHP.

## Examples

### Creating a TimeRange object
```php
// Create a new TimeRange
$timeRange1 = new TimeRange('2013-03-31 00:00:00', '2013-04-01 01:09:00');

// You can also use PHP DateTime objects
$start = new DateTime('2000-01-01');
$end = new DateTime('2000-01-05');
$timeRange2 = new TimeRange($start, $end);
```

### Looping TimeRange
TimeRange 0.1 supports looping minutes, hours, days and months.
```php
// Echo all days in time range
foreach ($timeRange1->getDays() as $datetime) {
  echo $datetime->format('Y-m-d')."<br>";
}

// Echo every other day in time range backwards
foreach ($timeRange1->getDays(2, TimeRange::BACKWARD) as $datetime) {
  echo $datetime->format('Y-m-d')."<br>";
}

// Echo all hours
foreach ($timeRange1->getMinutes() as $datetime) {
  echo $datetime->format('Y-m-d')."<br>";
}

```
