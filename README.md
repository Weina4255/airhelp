# Getting started:

go to the https://app.k6.io/
set up the K6 for your env https://k6.io/docs/getting-started/installation

Run the tests in CLI:

export let options = {
  ext: {
    loadimpact: {
      projectID: 3482640,
      name: "AirHelp"
    }
  }
}


Repo include two perfomance tests of the application: 

  * The test simulate the client behaviour of creating an orders: 
  ramp-up from 1 to 15 VUs in 2m, 
  stay at rest on 15 VUs for 3m,
  ramp-up from 15 to 10 000 VUs  for 2m,
  stay at rest 10 000 VUs for 5m,
  ramp-down from 10 000 to 0 VUs for 1m.

  * The test simulate the employee accept the created orders:
  ramp-up from 1 to 15 VUs in 2m, 
  stay at rest on 15 VUs for 3m,
  ramp-up from 15 to 10 000 VUs  for 2m,
  stay at rest 10 000 VUs for 5m,
  ramp-down from 10 000 to 0 VUs for 1m.
    
