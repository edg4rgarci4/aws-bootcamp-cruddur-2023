# Week 2 — Distributed Tracing
## Required Homework
- Watch [Week 2 Live-Stream Video](https://www.youtube.com/watch?v=2GD9xCzRId4&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=30) ✅
  - [Here](https://docs.google.com/document/d/1iUknCXVg_2Jfs7ARjydHcKprAFu6kp4gx9v519Hgjos/edit?usp=sharing) is a Google Doc of notes I took. 
- Watch Chirag [Week 2 - Spending Considerations](https://www.youtube.com/watch?v=2W3KeqCjtDY) ✅
  - Watched the video and did the spending quiz.
- Watched [Ashish's Week 2 - Observability Security Considerations](https://www.youtube.com/watch?v=bOf4ITxAcXc&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=31) ✅
  - [Here](https://docs.google.com/document/d/18PxGWexuZJaP_TOx0RF2gDqndTdflvo-NVQpkIkPQ4s/edit?usp=sharing) is a Google Doc of notes I took. I liked Chirag's Tom & Jerry analogy in explaining trace (gun powder trail).
- Instrument Honeycomb with OTEL ✅
  - Followed along [FREE AWS Cloud Project Bootcamp (Week 2) - Distributed Tracing video](https://www.youtube.com/watch?v=2GD9xCzRId4&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=30).
  - Commit is [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/643e0a018e1a9bd0dbc34da973809c377df4724c).
  - ![Honeycomb](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/blob/67d395ab1cae0e443de82f825322b7ef85e18e23/journal/assets/Week%202%20Honeycomb.png?raw=true)  
- Instrument AWS X-Ray ✅
  - Followed along [Week 2 Instrument XRay](https://www.youtube.com/watch?v=n2DTsuBrD_A&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=32) video.
  - Commit is [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/8ddfbe0e0c8c98962afd7ef6b57133f3c0d33d05).
- Instrument AWS X-Ray Subsegments ✅
  - Followed along [Week 2 - X-Ray Subsegments Solved](https://www.youtube.com/watch?v=4SGTW0Db5y0&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv) video.
  - Commit is [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/b486ebe2047801e2b3c06c102cefcb1dde48675b).
  - ![X-Ray Subsegments](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/blob/67d395ab1cae0e443de82f825322b7ef85e18e23/journal/assets/Week%202%20AWS%20X-Ray%20Subsegments.png?raw=true)
- Configure custom logger to send to CloudWatch Logs ✅
  - Followed along [Week 2 CloudWatch Logs](https://www.youtube.com/watch?v=ipdFizZjOF4&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=33) video.
  - Commit is [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/86106dea3d24af963ac5a7d24d9c35fa04e456fe).
- Integrate Rollbar and capture and error ✅	
  - Followed along [Week 2 - Rollbar](https://www.youtube.com/watch?v=xMBDAb5SEU4&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=35) video.
  - Commits are [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/04d8c233c937d150a6b3a38ba3d8d1e35c061bd8) and [here](https://github.com/edg4rgarci4/aws-bootcamp-cruddur-2023/commit/2d08f15a088ef00566f6ec4d4cc167f4da74ee72).
  - ![Rollbar New UI](https://user-images.githubusercontent.com/47645008/224196902-34166508-9536-426f-9ee0-e08aa769a4fd.png)
	
## Homework Challenges

### Suggested:
- Instrument Honeycomb for the frontend-application to observe network latency between frontend and backend[HARD]
- Add custom instrumentation to Honeycomb to add more attributes eg. UserId, Add a custom span ✅
- Run custom queries in Honeycomb and save them later eg. Latency by UserID, Recent Traces ✅
### Own:
- More research on Observability and OTEL
  - I poked around [Honeycomb's Youtube channel](https://www.youtube.com/@honeycombio). It was also good to spend time learning more about [OTEL](https://opentelemetry.io/). They had a video ([Instrumenting With OpenTelemetry](https://www.youtube.com/watch?v=Fb29Pw07gcY)) about this too. Lastly, I enjoyed watching and [Observability and the Glorious Future - Charity Majors](https://www.youtube.com/watch?v=babigcvGAXo) to build up and cement things that were covered by [Jessica](https://twitter.com/jessitron). I plan to watch [AWS re:Invent 2022 - Observability best practices at Amazon (COP343)](https://www.youtube.com/watch?v=zZPzXEBW4P8) next. 
