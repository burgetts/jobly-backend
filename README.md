# Jobly (backend)
This is the backend of the Jobly job board project. It is an API made using Express.js.

Deployed: https://web-production-d3f6.up.railway.app

## Routes
* /auth
  * [POST] /auth/token 
    * Login - receive token for user
  * [POST] /auth/register
    * Register - create user and receive token
* /companies
  * [POST] /companies (admin only)
    * Create new company
  * [GET] /companies 
    * Receive information on all companies (can filter by minEmployee, maxEmployee, and name)
  * [GET] /companies/:handle
    * Get information on a specific company by its handle
  * [PATCH] /companies/:handle (admin only)
    * Update information about a specific company by its handle
  * [DELETE] /companies/:handle (admin only)
    * Delete a specific company by its handle
* /jobs
  * [POST] /jobs (admin only)
    * Create a new job posting
  * [GET] /jobs
    * Receive information on all job postings
  * [GET] /jobs/:id
    * Get information on a specific job by its id
  * [PATCH] /jobs/:id (admin only)
    * Update information on a specific job by its id
  * [DELETE] /jobs/:handle (admin only)
    * Delete a specific job by its handle
* /users
  * [POST] /users (admin only)
    * Create a new user
  * [GET] /users (admin only)
    * Receive information on all users
  * [GET] /users/:username (admin or username only)
    * Get information on a specific user by their username
  * [PATCH] /users/:username (admin or username only)
    * Update user information for a specific user by their username
  * [DELETE] /users/:username (admin or usrname only)
    * Delete a specific user by their username
  * [POST] /users/:username/jobs/:id (admin or username only)
    * Allow a user to apply to a job by its id
