<!---
   Copyright 2017 Ericsson AB.
   For a full list of individual contributors, please see the commit history.

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
--->

# EiffelServiceDeployedEvent  (ServDe)
The EiffelServiceDeployedEvent is to declare when a configuration item/VM  and/or Service has been deployed by a machine/human.
It implies that the service is not in a running state and is ready to be started.

## Data Members
### data.servicename
__Type:__ String  
__Required:__ Yes  
__Description:__ The name of the Service that was deployed.

### data.instancename
__Type:__ String  
__Required:__ Yes  
__Description:__ The name of the instance that was deployed.

### data.owner
__Type:__ String  
__Required:__ Yes  
__Description:__ The entity that has been assigned/responsible for the Service.

### data.uri
__Type:__ String  
__Required:__ No  
__Description:__ A URI where further information can be obtained, if applicable. 

## Legal Link Types
### ENVIRONMENT
__Legal targets:__ [EiffelEnvironmentDefinedEvent](https://github.com/Ericsson/eiffel/blob/master/eiffel-vocabulary/EiffelEnvironmentDefinedEvent.md)  
__Multiple allowed:__ No  
__Description:__ Identifies the environment in which an event occurred, e.g. in which environment an artifact was built or an issue was verified.

### CONTEXT
__Legal targets:__ [EiffelActivityTriggeredEvent](https://github.com/Ericsson/eiffel/blob/master/eiffel-vocabulary/EiffelActivityTriggeredEvent.md), 
__Multiple allowed:__ No  
__Description:__ Identifies the activity of which the event constitutes a part. SHOULD not be used in conjunction with __CAUSE__, see above. Note that multiple layers may be modeled using __CONTEXT__, e.g. an activity being part of another activity.

### ACTIVITY_EXECUTION
__Legal targets:__ [EiffelActivityTriggeredEvent](https://github.com/Ericsson/eiffel/blob/master/eiffel-vocabulary/EiffelActivityTriggeredEvent.md)  
__Multiple allowed:__ No  
__Description:__ Declares the activity execution the event relates to. In other words, [EiffelActivityTriggeredEvent](https://github.com/Ericsson/eiffel/blob/master/eiffel-vocabulary/EiffelActivityTriggeredEvent.md) acts as a handle for the activity execution. This differs from __CONTEXT__. In __ACTIVITY_EXECUTION__ the source carries information pertaining to the target (i.e. the activity started, finished or was canceled). In __CONTEXT__, on the other hand, the source constitutes a subset of the target.

## Version History
| Version   | Introduced in                                          | Changes                                 |
| --------- | ------------------------------------------------------ | --------------------------------------- |
| 1.0.0     |                                                        | Initial version.                        |

## Examples
