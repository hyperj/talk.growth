# Moment Record

**yarn container_id format**

```java
// ContainerId represents a globally unique identifier for a Container in the cluster.
// The format is container_e*epoch*_*clusterTimestamp*_*appId*_*attemptId*_*containerId*
// *epoch* is increased when RM restarts or fails over. When epoch is 0, epoch is omitted
ApplicationId applicationId = ApplicationId.newInstance(timestamp, appId);
ApplicationAttemptId applicationAttemptId = ApplicationAttemptId.newInstance(applicationId, appAttemptId);
ContainerId containerId = ContainerId.newContainerId(applicationAttemptId, containerId);
```