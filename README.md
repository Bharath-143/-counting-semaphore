 Queue<process> a; 
  
} P(Semaphore d) 
{ 
    d.value = d.value - 1; 
    if (d.value < 0) { 
  
        a.push(p); 
        block(); 
    } 
    else
        return; 
} 
  
V(Semaphore d) 
{ 
    d.value = d.value + 1; 
    if (d.value <= 0) { 
  
        a.pop(); 
        wakeup(p); 
    } 
    else
        return; 
} 
