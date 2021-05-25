# Objective:
  ## Create an application for your restaurant that allow users to make and modify reservations.
  
# Git Requirements:
  - [ ] Your code should be committed frequently and pushed at the end of each working session (never leave unpushed code overnight).
  - [ ] Do NOT work in the Master (Dev) branch EVER. Create a separate feature branch for each "feature" as you implement it, then merge when you have a working feature. (SEE GIT INSTRUCTIONS BELOW)

# Code Requirements:
  - [ ] Your code should follow the single-responsibility principle of the SOLID methodology and should follow the inheritance and encapsulation pillars of APIE (OOP).
  - [ ] There should only ever be 1 instance of your restaurant. Include logic that prevents creating a second restaurant. (Singleton Pattern)
  - [ ] Allow guests to get an alert 1 hour before their scheduled reservation. (Observer Pattern)
  - [ ] Reservations should be generated from a reservation class that can consistently generate new reservation objects as needed. (Factory Pattern)
  - [ ] Accept reservations as objects that get stored in the restaurant object. (Mediator Pattern)


# Functionality Requirements:
  - [ ] Should be able to create a new reservation, edit a reservation, and delete a reservation.
  - [ ] You should know how many customers you can accommodate at once. Do not allow reservations to exceed your max capacity.
  - [ ] Each reservation should have a 1 hour time slot (for simplicity).
  - [ ] Your restaurant should be closed at least 1 day a week.
  - [ ] Your restaurant should have normal hours (you can pick your own hours).
  - [ ] Your restaurant should have extended hours as well (see example below).

# Example Restaurant Hours:
```
  Mon: closed
  Tues: 5pm - 10pm  (normal hours)
  Wed: 5pm - 10pm  (normal hours)
  Thu: 5pm - 10pm  (normal hours)
  Fri: 5pm - 12am  (extended hours)
  Sat: 5pm - 12am  (extended hours)
  Sun: 5pm - 10pm  (normal hours)
```

# Example Directory:
```
restaurant/
  js/
    helperClasses/
      calendarHelper.js
      observerHelper.js
      singletonHelper.js
      tableHelper.js
    app.js
    library.js (optional)
    restaurant.js
  index.html
  ```

# Assumptions:
  - Assume that all reservations will start and end exactly as scheduled. We will assume no customers are late.
  - Assume that we are open on holidays during normal business hours (whatever you set in your restaurant hours).
  - Assume that you will not have any walk-in guests - all guests must make a reservation.
  - Assume that every guest will have exactly the number of people listed in the reservation (no extra people, no missing people).

# GIT Instructions:
  commits should be at least every 30 minutes, even if code isn't working (avoid pushing code that isn't working, but committing is fine)
  
  if you added a new file since your last commit:
```
    $ git add .
    $ git commit -m "message"
```
  if you did not add any new files since your last commit:
```
    $ git commit -am "message"
```

  You only need to push code at the end of each working session (not required after every commit). Do not leave uncommitted code overnight.
  
  Normally you would do a pull request, but since it's a solo project, you can just merge when you're ready.
  To merge your feature branch to master (dev):
```
    $ git checkout dev
    $ git merge feature/my-branch
```

  After merging, you will need to delete your previous branch. You can do this easily in GitHub directly, otherwise, you can do this:
```
    $ git branch -d feature/my-old-branch
```

  After merging you will be required to create a new branch. This is easiest to do in GitHub directly as it will set the upstream origin for you.
  If you created a new feature branch in GitHub, then do:
```
    git fetch
    git checkout feature/my-new-branch
```

  If you are creating a new feature branch through your bash terminal:
```
    git checkout -b feature/my-new-branch
    git push -u origin feature/my-new-branch
```
  
