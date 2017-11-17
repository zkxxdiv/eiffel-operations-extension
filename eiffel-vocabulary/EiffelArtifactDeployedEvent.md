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

# EiffelArtifactDeployedEvent (ArtD)
The EiffelArtifactDeployedEvent id to declare that an artifact has been deployed into an environment.

## Data Members

### data.uri
__Type:__ String  
__Required:__ No  
__Description:__  A URI where further information can be obtained, if applicable.

## Legal Link Types
### CAUSE
__Legal targets:__ Any  
__Multiple allowed:__ Yes  
__Description:__ Identifies a cause of the event occurring. SHOULD not be used in conjunction with __CONTEXT__: individual events providing __CAUSE__ within a larger context gives rise to ambiguity. It is instead recommended to let the root event of the context declare __CAUSE__.  

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
