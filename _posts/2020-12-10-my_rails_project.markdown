---
layout: post
title:      "My Rails Project"
date:       2020-12-10 11:28:08 -0500
permalink:  my_rails_project
---


My rails application has been my biggest hurdle as far as projects go. I did a double nested form for my rails project. I learned quite a bit along the way but it was not easy. These articles helped me understand nested forms and nested attributes. 
•	https://levelup.gitconnected.com/the-many-things-about-nested-form-in-ruby-on-rails-15f32ed66446
•	https://www.sitepoint.com/complex-rails-forms-with-nested-attributes/

I also ran into an issue with my application, instead of editing a patient’s medications, my project was adding new prescriptions to a patient. It turns out my strong params was missing an ID so it was adding a new medication instead of editing the medication. 

Here is what my code initially looked like:
params.require(:patient).permit(:name, illnesses_attributes: [:illness, :patient_id, :medication_id, medication_attributes: [:name, :frequency, :quantity]])

When I updated the params to include the illness id, then my application successfully would edit the medication instead of adding a new medication. 
params.require(:patient).permit(:name, illnesses_attributes: [:id, :illness, :patient_id, :medication_id, medication_attributes: [:id, :name, :frequency, :quantity]])

