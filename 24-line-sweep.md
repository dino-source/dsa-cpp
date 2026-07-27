# LeetCode Pattern: Line Sweep

## Overview

The Line Sweep pattern is used to solve problems involving intervals,
events, and overlapping ranges.

The main idea is to convert continuous changes into discrete events and
process them in sorted order.

Instead of checking every point on a timeline:

```text
Brute force:

Check every moment:

0 1 2 3 4 5 6 7
```

we only process moments where something changes:

```text
Events:

start
end
start
end
```

Line Sweep is especially useful for:

- interval overlaps;
- meeting schedules;
- active ranges;
- computational geometry;
- counting simultaneous events.

The typical approach:

1. Convert intervals into events.
2. Sort events by position.
3. Sweep from left to right.
4. Maintain the current state.

In C++, this pattern commonly uses:

- `std::vector`;
- `std::sort`;
- priority queues;
- maps for ordered events.

The key skill is recognizing when a problem asks about what happens while
moving through a timeline.

---

## Practice Problems

Solve these problems in order. The early problems introduce interval
processing, while the later ones require more advanced sweep techniques.

### Easy

- **56. Merge Intervals**  
  <https://leetcode.com/problems/merge-intervals/>

  Sort intervals and merge overlapping ranges.

- **252. Meeting Rooms**  
  <https://leetcode.com/problems/meeting-rooms/>

  Determine whether any meetings overlap.

### Medium

- **57. Insert Interval**  
  <https://leetcode.com/problems/insert-interval/>

  Insert and merge a new interval efficiently.

- **253. Meeting Rooms II**  
  <https://leetcode.com/problems/meeting-rooms-ii/>

  Count the minimum number of rooms required for all meetings.

- **435. Non-overlapping Intervals**  
  <https://leetcode.com/problems/non-overlapping-intervals/>

  Remove the minimum number of intervals to eliminate overlaps.

- **729. My Calendar I**  
  <https://leetcode.com/problems/my-calendar-i/>

  Track booked intervals and reject conflicting events.

- **731. My Calendar II**  
  <https://leetcode.com/problems/my-calendar-ii/>

  Allow double bookings but prevent triple bookings.

### Hard

- **218. The Skyline Problem**  
  <https://leetcode.com/problems/the-skyline-problem/>

  Use a sweep line with a heap to process building boundaries.

- **759. Employee Free Time**  
  <https://leetcode.com/problems/employee-free-time/>

  Find common free time among multiple schedules.

- **850. Rectangle Area II**  
  <https://leetcode.com/problems/rectangle-area-ii/>

  Apply advanced sweep techniques to compute union area.

---

## Pattern Recognition Checklist

Ask yourself:

- Does the problem involve intervals or ranges?
- Do I need to know how many events are active at a certain point?
- Can I represent changes as start/end events?
- Would sorting all events simplify the problem?
- Am I dealing with overlapping timelines?

If yes, Line Sweep is likely a strong candidate.

---

## Common Interview Keywords

Look for phrases like:

- "interval";
- "overlap";
- "intersection";
- "schedule";
- "timeline";
- "events";
- "maximum number of";
- "active";
- "simultaneously".

---

## Common Line Sweep Variations

### Basic Interval Sweep

Convert intervals into sorted ranges.

Example:

```text
Intervals:

[1, 5]
[3, 7]

After sorting:

[1, 5]
[3, 7]

Overlap:

[1, 7]
```

Typical examples:

- Merge Intervals
- Insert Interval

---

### Event-Based Sweep

Convert each interval into two events.

Example:

```text
Meeting:

[2, 5]


Events:

2 -> start
5 -> end
```

Process events in order:

```text
time:  2 3 4 5

rooms:
      1 1 1 0
```

Typical examples:

- Meeting Rooms II
- My Calendar II

---

### Sweep Line + Heap

Maintain active intervals using a priority queue.

Example:

```text
Heap contains:

end times of active meetings
```

When a meeting ends:

```text
remove finished intervals
```

Typical examples:

- Meeting Rooms II
- The Skyline Problem

---

### Sweep Line + Coordinate Compression

When coordinates are very large:

```text
1,000,000,000
```

cannot be processed directly.

Compress coordinates:

```text
1, 500, 1000000000

becomes:

0, 1, 2
```

Typical examples:

- Rectangle Area II
- Falling Squares

---

## Complexity

Most Line Sweep solutions require sorting events.

Typical complexity:

- Time complexity: `O(n log n)`
- Space complexity: `O(n)`

The sorting step usually dominates the runtime.

For advanced geometry problems:

- Time complexity may depend on the number of events;
- Additional data structures may increase complexity.

---

## Learning Goals

After completing this pattern, you should be able to:

- recognize interval and timeline problems;
- convert ranges into events;
- implement basic sweep line algorithms;
- combine sweep line with heaps;
- handle large coordinate ranges using compression.

---

## Progress

- [ ] 56. Merge Intervals
- [ ] 252. Meeting Rooms
- [ ] 57. Insert Interval
- [ ] 253. Meeting Rooms II
- [ ] 435. Non-overlapping Intervals
- [ ] 729. My Calendar I
- [ ] 731. My Calendar II
- [ ] 218. The Skyline Problem
- [ ] 759. Employee Free Time
- [ ] 850. Rectangle Area II
