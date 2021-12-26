---
layout: post
title: Monty Hall Simulation 
image: "/posts/monty_hall.jpg"
tags: [Tableau, Dashboard]
---
I used Python to create a simulation of teh monty hall challenge which the show "Let's Make a Deal' is based on. Switching creates about a 66% or 2/3 of a chance for success, as opposed to staying, as it only has a 33% or 1/3 chance of success.

---

![alt text](/img/posts/monty_hall_post.png "Monty Hall")


```ruby
import random



def monty_hall(trials): 
    stay_wins = 0
    stay_loss = 0
    switch_wins = 0
    switch_loss = 0
    for x in range(trials):
        doors = ['goat', 'car', 'goat']
        stay_or_switch = ['stay', 'switch']
        door_choice = random.choice(doors)
        stay_or_switch = random.choice(stay_or_switch)
        if stay_or_switch == 'stay':
            if door_choice == 'car':
                #print('Stay is successful. You won a car')
                stay_wins += 1
            else:
                stay_loss += 1
                #print('Stay is unsuccessful. You lost')
        elif stay_or_switch == 'switch':
            if door_choice == 'car':
                #print('Switch is successful. You won a car')
                switch_loss += 1
            if door_choice == 'goat':
                switch_wins += 1
                #print('Switch is unsuccessfull. You lost')

    total_stay_win_perc = int((stay_wins/(stay_wins+stay_loss) * 100))
    total_switch_win_perc = int((switch_wins/(switch_wins+switch_loss) * 100))
    print(f'Amount of Stay wins is {stay_wins}')
    print(f'Amount of Stay losses is {stay_loss}')
    print(f'Amount of Switch wins is {switch_wins}')
    print(f'Amount of Switch losses is {switch_loss}')

    
    print(f'Stay has a win percentage of {total_stay_win_perc}%')
    print(f'Switch has a win percentage of {total_switch_win_perc}%')
    
```

