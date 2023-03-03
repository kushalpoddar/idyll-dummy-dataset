# idyll-dummy-dataset

This repository contains two files - users.csv and swipes.csv.

users.csv - Dataset of ~ 1400 users with parameters which can be self understood. Some parameters may need explanation which is described below.

  is_verified - If the account is verfied or not. We give a yellow tick to users with verfied profiles. This is done manually by our representatives by matching id cards with their actual information.

  status - If it is false, user may access his/her profile but this wont be visible to user users. Status false is done in situations where our representatives manually makes it false due to fake photos upload, fake information upload, etc.

  _id - Unique primary key of the user
   
  face_detection_probabilities - Can be ignored.
  
  who_to_date - F (Female), M (Male), A (Anyone)
  
Some profiles might not have all information because users dropped off in between. The email ids and mobile numbers are masked and generated automatically to preserve their real identity.

swipes.csv - Dataset of ~60k swipes by profiles.
  
  id - Primary ID of the swipe or match
  
  p1 - Primary ID of the first person performing the swipe. If A swipes B then p1 is A
  
  p2 - Primary ID of the person who was swiped by p1. If A swipes B then p2 is B
  
  first_type - LIKE or DISLIKE performed by p1
  
  is_unmatch - If the match was unmatched by any user.
  
  unmatch_on - Timestamp of unmatch
  
  like_count - 1 if single swipe is done. 2 if both have swiped each other
  
  second_type - LIKE or DISLIKE performed by p2 (Only present if like_count is 2) and 2nd user performed the action.
  
  p1_extend_at and p2_extend_at are irrelevant. 
  
