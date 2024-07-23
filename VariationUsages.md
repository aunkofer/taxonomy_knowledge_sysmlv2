# A SysML v2 'Variation Usages' Example using textual sysml v2 notation

'''

package 'Variation Usages' {
	import 'Variation Definitions'::*;
	
	part def Vehicle;
	part def Transmission;
	part manualTransmission;
	part automaticTransmission;
	
	abstract part vehicleFamily : Vehicle {
		part engine : EngineChoices[1];
		
		variation part transmission : Transmission[1] {
			variant manualTransmission;
			variant automaticTransmission;
		}
		
		assert constraint {
			(engine == engine::'4cylEngine' and
			 transmission == transmission::manualTransmission) xor
			(engine == engine::'6cylEngine' and 
			 transmission == transmission::automaticTransmission)
		}	
	}
	
}

'''

