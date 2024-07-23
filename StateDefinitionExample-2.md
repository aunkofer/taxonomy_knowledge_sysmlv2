# A SysML v2 'State Definition Example' using textual sysml v2 notation

'''

package 'State Definition Example-2' {
	
	attribute def VehicleStartSignal;
	attribute def VehicleOnSignal;
	attribute def VehicleOffSignal;
		
	state def VehicleStates {
		entry; then off;
		
		state off;
		accept VehicleStartSignal 
			then starting;
			
		state starting;
		accept VehicleOnSignal
			then on;
			
		state on;
		accept VehicleOffSignal
			then off;
	}
	
}

'''
