# Entity-relationship-model-Checkpoint


Entities and Their Attributes
1. Gymnasium
gym_id (Primary Key)

name

address

phone_number

2. Member
member_id (Primary Key)

last_name

first_name

address

date_of_birth

gender

gym_id (Foreign Key → Gymnasium)

3. Coach
coach_id (Primary Key)

last_name

first_name

age

specialty

4. Session
session_id (Primary Key)

sport_type

schedule

gym_id (Foreign Key → Gymnasium)

Relationships
1. Registration (Member ⬌ Session)
A member can register for multiple sessions.

A session can have up to 20 members.

Attributes: none (just a many-to-many relationship)

Associative Entity: Registration(member_id, session_id) with a constraint to not exceed 20 members per session.

2. Conduct (Coach ⬌ Session)
A session can be led by up to two coaches.

A coach can conduct multiple sessions.

Associative Entity: Conducts(coach_id, session_id) with a constraint to not exceed 2 coaches per session.
