# Interview Questions
## Fundamentals
> Graceful degradation
* Graceful degradation allows non-critical functionality to continue operating even when some services fail. Restarting servers or disabling caches increases downtime. Modern resilient systems prioritize partial functionality over complete failure.

> Resilient vs Fault Tolerance
* Resilient: broader ability to absorb disruption, degrade gracefully, recover and return to normal
    * resistance + graceful degradation + containment + recovery 
* Fault Tolerance: The ability to keep operating correctly while a component is failing
    * Fault tolerance is usually one technique within resilience
    * continued correct operation despite specific faults 

> Circuit breaker
* The Circuit Breaker pattern prevents cascading failures by temporarily stopping requests to unhealthy services. Infinite retries can worsen outages. Restarting databases or permanently blocking users are poor operational strategies. This pattern is frequently discussed in system design interviews.