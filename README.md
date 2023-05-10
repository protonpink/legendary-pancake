

## The Tech 


### Wireframing
Link to Live View : https://www.figma.com/proto/KjxNiK5o2mjUIZ5GEQl4gp/Buddy?page-id=0%3A1&node-id=2-39&viewport=591%2C324%2C0.15&scaling=scale-down&starting-point-node-id=2%3A39

Link to the WireFraming Structure: https://www.figma.com/file/KjxNiK5o2mjUIZ5GEQl4gp/Buddy?node-id=0%3A1&t=xO6d3bfAkWkzdWyv-1


### User Stories 
Link : https://miro.com/app/board/o9J_ktbE4yk=/?share_link_id=713979444829

### MVP
- landing page (inc: mission statement, app title, (hard coded success story) footer, navigation)
- sign up entry point (redirect to using auth). 
- select either international, local user type.
- register for the site
- view confirmation page
- click to view gallary of other (international / local)
- filter view by international / local
 

### Stretch
- additional filters on gallary page e.g. languages?
- view user profile
- ability to email selected user
- email form 
- cute confirmation that email is sent
- carosel for success stories viewable on landing page. 

-------

## Views (Client Side)
| name | purpose |
| --- | --- |
| Home| Welcome registered/unregistered users and display links to other parts of the site |
| CreateProfileForm | view for international or local users to sign up |
| Personal details | View for the personal details of the user |
| All Profiles | View for displaying all the profiles of international/local |
| EditProfileForm | View for user to update their details about themselves |


## Reducers (Client Side)
| name | purpose |
| --- | --- |
| InternationalReducer | Store the array of International users (from db) |
| LocalReducer | Store the array of Local users (from db) |

## Actions (Client Side)

### International 
| type | data | purpose |
| --- | --- | --- |
| SET_INTUSERS | User[] | Retrieve all international and local users from the db and store in redux |
| GET_INTUSERS | User | Ret individual international user from the db and store in redux |
| DEL_INTUSER| number | Delete individual international user from db |
| ADD_INTUSER | User | Add individual international user to the db  |
| UPDATE_INTUSER | User | Update individual international |
| SHOW_ERROR | string | |

### Local 
| type | data | purpose |
| --- | --- | --- |
| SET_LOCALUSERS | User[] | Retrieve all international and local users from the db and store in redux |
| GET_LOCALUSERS | User | Retrieve individual international or local users user from the db and store in redux |
| DEL_LOCALUSER| number | Delete individual international or local user from db |
| ADD_LOCALUSER | User | Add individual international or local user to the db |
| UPDATE_LOCALUSER | User | Update individual international or local user to db  |
| SHOW_ERROR | string | -- | 



## API (Client - Server)

| Method | Endpoint | Protected | Usage | Response |
| --- | --- | --- | --- | --- |
| Get | /api/v1/buddy | Yes | Get the list of all the users | Array of Objects (object = users) |
| Get | /api/v1/buddy/:id | Yes | Get single user data by id | A single Object (object = userData by id) |
| Post | /api/v1/buddy/ | Yes | Save a completed new user data profile| the data that has been saved in db read format |
| Delete | /api/v1/buddy/:id | Yes | Delete a user data profile| Delete from db by Id |
| Patch | /api/v1/buddy/:id | Yes | Update a user data profile | Update the User data by Id in db|



## DB (Server Side) 
  There should be one table for MVP.
  
### users
  | Column Name | Data Type | Purpose |
  | --- | --- | --- |
  | id | Integer | Unique identifier for each international and local users|
  | user_name | String | user name users when they are done signing up through Auth0|
  | first_name | String | First Name of the user as personal detail |
  | last_name | String | Last Name of the user as personal detail  |
  | email | String | Contact email of the user which will be used for the communication|
  | age | String | Age of the user as personal detail |
  | country_origin | String | User's country origin as personal detail |
  | city | String | City where the user come from as personal detail |
  | user_status | String | Whether the user is international or local, It will be two values: International or Local |
  | prim_language | String | Their primary language speaking everyday|
  | english_level | String | How good their english leve, It will be three values: no english, some english, and fluent english |
  | sharing_one | String | User's Interest Both for Local and International |
  | sharing_two | String | User's Interest Both for Local and International  |
  | sharing_three | String | User's Interest Both for Local and International |
  | description | String | User's Short Bio Both for Local and International |
  | profile_img | String | User's profile picture Both for Local and International |
  | auth_id | String | to validate Users because we are using Auth0|
  
  


### unsplash image collection
https://unsplash.com/collections/-QfwWYXM4UQ/buddy





