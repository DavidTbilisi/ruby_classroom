## TASK 1 — Print numbers 1..x → `output1`

### Variant A — `upto`

```ruby
output1 = ""
1.upto(x) { |num| output1 << "#{num} " }
output1 = output1.strip
```

### Variant B — `while`

```ruby
output1 = ""
i = 1
while i <= x
  output1 << "#{i} "
  i += 1
end
output1 = output1.strip
```

### Variant C — Range + join

```ruby
output1 = (1..x).to_a.join(" ")
```

---

## TASK 2 — Even numbers 1..20 → `output2`

### Variant A — `step`

```ruby
output2 = ""
2.step(20, 2) { |n| output2 << "#{n} " }
output2 = output2.strip
```

### Variant B — `while`

```ruby
output2 = ""
i = 1
while i <= 20
  output2 << "#{i} " if i.even?
  i += 1
end
output2 = output2.strip
```

### Variant C — `select`

```ruby
output2 = (1..20).select(&:even?).join(" ")
```

---

## TASK 3 — Sum 1..50 using `while` → `total = 1275`

### Variant A

```ruby
total = 0
i = 1
while i <= 50
  total += i
  i += 1
end
```

### Variant B — reverse

```ruby
total = 0
i = 50
while i >= 1
  total += i
  i -= 1
end
```

---

## TASK 4 — Factorial of 10 → `fact = 3628800`

### Variant A — loop

```ruby
fact = 1
i = 1
while i <= n
  fact *= i
  i += 1
end
```

### Variant B — `downto`

```ruby
fact = 1
n.downto(1) { |k| fact *= k }
```

### Variant C — functional

```ruby
fact = (1..n).inject(1, :*)
```

---

## TASK 5 — Print "OK" 5 times → `output5`

### Variant A

```ruby
output5 = ""
5.times { output5 << "OK " }
output5 = output5.strip
```

### Variant B

```ruby
output5 = (["OK"] * 5).join(" ")
```

---

## TASK 6 — Numbers 30 down to 15 → `output6`

### Variant A

```ruby
output6 = ""
30.downto(15) { |num| output6 << "#{num} " }
output6 = output6.strip
```

### Variant B

```ruby
output6 = ""
i = 30
while i >= 15
  output6 << "#{i} "
  i -= 1
end
output6 = output6.strip
```

---

## TASK 7 — First number divisible by 17 (1..100) → `result = 17`

### Variant A

```ruby
result = nil
(1..100).each do |i|
  if i % 17 == 0
    result = i
    break
  end
end
```

### Variant B

```ruby
i = 1
while i <= 100
  if i % 17 == 0
    result = i
    break
  end
  i += 1
end
```

### Variant C

```ruby
result = (1..100).find { |i| i % 17 == 0 }
```

---

## TASK 8 — Count numbers divisible by 3 AND 5 (1..200) → `count`

### Variant A

```ruby
count = 0
(1..200).each { |i| count += 1 if i % 15 == 0 }
```

### Variant B

```ruby
count = (1..200).count { |i| i % 15 == 0 }
```

---

## TASK 9 — "Ruby!1" .. "Ruby!7" → `output9`

### Variant A

```ruby
output9 = (1..7).map { |i| "Ruby!#{i}" }.join(" ")
```

### Variant B

```ruby
output9 = ""
1.upto(7) { |i| output9 << "Ruby!#{i} " }
output9 = output9.strip
```

---

## TASK 10 — Sum odd numbers 1..40 → `odd_sum`

### Variant A

```ruby
odd_sum = 0
(1..40).each { |n| odd_sum += n if n.odd? }
```

### Variant B

```ruby
odd_sum = (1..40).select(&:odd?).sum
```

---

## TASK 11 — Countdown 5..1 then "GO!" → `output11`

### Variant A

```ruby
output11 = ""
5.downto(1) { |t| output11 << "T-minus #{t}" }
output11 << "GO!"
```

---

## TASK 12 — Build stars → `stars = "****"`

### Variant A

```ruby
stars = ""
4.times { stars << "*" }
```

### Variant B

```ruby
stars = "*" * 4
```

---

## TASK 13 — Numbers 1..30, skip divisible by 4 → `output13`

### Variant A

```ruby
output13 = ""
(1..30).each do |i|
  next if i % 4 == 0
  output13 << "#{i} "
end
output13 = output13.strip
```

---

## TASK 14 — Multiply by 2 until ≥ 1000 → `x2`

### Variant A

```ruby
x2 = 1
while x2 < 1000
  x2 *= 2
end
```

---

## TASK 15 — Dashed string "ruby" → `"r-u-b-y-"`

(no arrays, no `.chars`)

### Variant A

```ruby
dashed = ""
i = 0
while i < str.length
  dashed << str[i] << "-"
  i += 1
end
```

---
* Turn this into a **cheat sheet for students**
