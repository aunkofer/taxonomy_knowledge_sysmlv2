# A SysML v2 'State Exhibition Example' using textual sysml v2 notation

'''

package 'State Exhibition Example' {
	import 'Transition Actions'::*;
	
	part vehicle : Vehicle {
		
		part vehicleController : VehicleController;
		
		exhibit vehicleStates {
			in operatingVehicle = vehicle;
			in controller = vehicleController;
		}

	}
	
}

'''
