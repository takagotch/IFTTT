### IFTTT
---
https://github.com/IFTTT

#### feedjira
https://github.com/IFTTT/feedjira

```rb
// lib/feedjira/core_ext/date.rb
class Date
  def feed_utils_to_gm_time
    feed_utils_to_time(new_offset, :gm)
  end
  
  def feed_utils_to_local_time
    feed_utils_to_time(new_offset(DateTime.now.offset-offset), :local)
  end
  
  private
  def feed_utils_to_time(dest, method)
    Time.send(method, dest.year, dest.month, dest.day, dest.hour, dest.min,
      dest.sec, dest.zone)
  end
end

```

```
```

```
```


