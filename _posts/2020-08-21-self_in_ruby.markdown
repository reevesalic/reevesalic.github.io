---
layout: post
title:      "Self in Ruby"
date:       2020-08-21 16:27:46 -0400
permalink:  self_in_ruby
---


Self is a BIG topic. I will try to keep it short and concise. Self in Ruby means you have access to the current object. The current object is what is receiving the current message. Self can used to refer to a class. Self can be used in the initialize method and it can be used in an instance method. 

1. Initialize Method – Self refers to the new instance of the class. 
    
    Example:
		
    ```
   def initialize (cat)
    @cat = cat
    @@all << self
    End 
```
		
2. Class –Self in a class refers to the class itself.
    
	  Example:
		
    ```
 def self.all
     @@all
     end
```

3. 	Instance Method –  self refers to the instance the method is being called on. When you do not explicitly  use self in          your method, it is assumed. 
     
	   Example:
		 
     def car
     puts “The car is fast.”
     end

Thanks!
Alicia Reeves
