# A SysML v2 'Individuals and Time Slices' Example using textual sysml v2 notation

'''

package 'Individuals and Time Slices' {
	import 'Individuals and Snapshots Example'::*;
	
	individual item def Alice :> Person;
	individual item def Bob :> Person;
	
	individual : Vehicle_1 {
		
		timeslice aliceDriving {
			ref individual item :>> driver : Alice;

			snapshot :>> start {
				:>> mass = 2000.0;
			}
			
			snapshot :>> done {
				:>> mass = 1500.0;
			}			
		}
		
		then timeslice bobDriving {
			ref individual item :>> driver : Bob;
		}
		
	}
}

'''
