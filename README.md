# User service

We want you to write a very simple `User` web service. Depending on your experience, the typical effort for this should be **1-8 hour(s)**.
If it does take longer, feel free to take your time, but it is not our intention to cut off that much free time from you.

Please use any programming languge / libraries / frameworks that you are **most comfortable** with.

Please make sure that you meet the acceptance criteria. It would be nice to implement some of the bonus criteria.

**Hint:** we prefer simple solutions over complex ones.

## Requirements

- The service should implement a JSON REST interface
- A `User` has a `username` a `password` and a `role` (`admin` or `ordinary`)
- For `admin` users it should be possible
  - add new users
  - delete existing users
  - update user's passwords
- For `ordinary` users it should be possible to 
  - list all user's and their associated roles
  - update their own password
- All endpoints should be protected via an `X-API-TOKEN` header
- A token can be obtained by an unprotected login endpoint, where a valid `username` and `password` returns a valid token

## Acceptance Criteria

- The service must meet all of the above mentioned requirements
- There is a `README.md` that documents how to build and run the service
- The source code builds and runs
- There are no errors or crashes

## Bonus Criteria

- [ ] A token should only be valid for a **configurable** amount of seconds
- [ ] The service has a valid [Open API](https://www.openapis.org/) description
- [ ] The service persists the user data and the data is not lost during reboot of the application
- [ ] The service is stored in a private GitHub repository shaed with [@cinemast](https://github.com/cinemast)
- [ ] The service has a CI/CD pipeline which automatically builds and tests the service
- [ ] There are automated integration tests which can be run
- [ ] The service can easily be started via a `docker-compose` command
- [ ] The service is public available on the internet (there are many free options for trial accounts that allow free hosting of your service)
- [ ] The service is public available via `https`
- [ ] There is a **very minimalistic** front-end deomnstrating the functionality of the user service, it does not need to be pretty at all.

## Questions worth considering

- Under what circumstances will your service fail to work?
- What happens with a valid token if the associated user has been deleted?
- Can a user have multiple tokens?
- Could this be implemented in a more simple way?
- How big is the deployed application and could it be smaller?
