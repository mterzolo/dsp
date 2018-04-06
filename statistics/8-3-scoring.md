[Think Stats Chapter 8 Exercise 3](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77)

---

def sim_game(lam):
    
    goals = 0
    time = 0
    
    while time <= 1:
        
        time_to_goal = random.expovariate(lam)
        
        time += time_to_goal
        
        goals += 1
        
    return goals

def many_games(lam, num_experiments):
    
    estimates = [sim_game(lam) for i in range(0,num_experiments)]
    
    mean_error = MeanError(estimates, lam)
    
    rmse = RMSE(estimates, lam)
    
    return mean_error, rmse

---
