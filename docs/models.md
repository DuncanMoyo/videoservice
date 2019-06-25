###MODEL ARCHITECTURE PLANNING****

Membership
    - slug
    - type (free, ent, pro)
    - price
    - stripe plan id

UserMembership
    - User                      (foreignkey to default user)
    - stripe customer id
    - membership type           (foreignkey to Membership)
    
Subscription
    - user membership
    - stripe subscription id    (foreignkey to User membership)
    - active

Course
    - slug
    - title
    - description
    - allowed memberships       (foreignkey to Membership)

Lesson
    - slug
    - title
    - course                    (foreignkey to Course)
    - position
    - video
    - thumbnail