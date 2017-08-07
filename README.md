# ISX-2250-Africa-Delete
The ISX 2250 South Africa Delete Project.


Official Project Version "E".

  This is the "South Africa Delete (S.A.D.)" project file collection. It
consists of this read-me and generic overlay. Instructions for use are
as follows, use at own risk.

. Overlay is only intended for use with the 'BBZ' version of the 2250
  engine.

. Overlay is only for use with Incal files and not meant for existing
  engine files taken from running engine.

. Overlay is not compatible with other overlays or deletes.

--== Instructions for use ==-

+ Read entire document well and establish good understanding of the
  process.

+ Extract the proper Incal file for the engine according to its CPL. Do
  not jump CPL!.

+ Use Calterm with proper meta-file to perform overlay onto extracted
  file.
  
	WARNING: DO NOT OPEN EXTRACTED INCAL FILE TO EDIT/SAVE IT IN
	CALTERM!. Often, this will alter some of the header and other
	informations inside the Incal file and deteriorates its integrity.
	Sometimes causes issues with the ecm. Performing only the overlay
	does not cause this issue. Only do overlay!. If parameter editing is
	desired then the file can be taken from the truck and edited after
	the re-flashing process.
	
+ Compress the Incal file as it was and place it into proper folder so
  that the file can be flashed into the ecm with Insite.
  
+ Unplug all hardware electrical connectors for all NOx sensors, SCR
  controller, egr valve, and all other egr and emissions related
  sensors.

    WARNING: Everything must be unplugged or the ecm will re-establish
    J1939 communications to the devices such as the egr valve or NOx
    sensors and flag them with errors.
   

+ Use standard methods to flash the file into the ecm with Insite. Be
  sure to make an ecm image in Insite beforehand so that settings do not
  get lost.

+ After flash is complete, run the engine for at least 10 minutes so
  that it can establish settings in RAM memory of the ecm before
  continuing.

	NOTE: The ecm will only perform a proper clean "first boot" when
	flashed with an Incal file via the Insite software. Calterm is not
	capable of making this happen. Calterm will very often remove/alter
	this process by mistake when saving an incal file. This is why it is
	important not to edit any incal file using Calterm and also to wait
	10 minutes with first engine startup after an ecm re-flash.
		
	
+ After 10 minutes of initial engine run time the ecm file can be
  uploaded to/from the truck directly with Calterm and altered/edited
  if needed or desired. Never edit incal file directly.

+ A blocking plate can be used between the exhaust manifold and the egr
  cooler at its elbow joint if desired. The plate must be made of thick
  stainless and able to withstand exhaust pressures in excess of 184
  inhg (90 psig). Coolant flow through the egr cooler circuit must not
  be blocked so that coolant will move through the rear half of the
  engine properly. A 19mm (3/4") hose should replace the egr cooler
  coolant circuit if it is to be removed. A second plate can be
  installed at the egr mixing joint of the intake as well to prevent lag
  or leakage of boost pressure.

+ All exhaust components must be removed or modified and made 100%
  hollow. This includes the SCR component as it will clog up over time.
  
	NOTE: No component should be left partially intact so that it can
	absorb or reflect exhaust gas heat. Shortened engine and
	turbocharger life will result.


+ Altering egr and exhaust components directly effects turbocharger
  operation. It is necessary to test drive the equipment placing it
  under full engine operating load and checking maximum achieved
  turbocharger boost pressure to ensure it is not in excess. Maximum
  turbocharger pressure should not exceed 74 inhg (36 psig) no matter
  the Horsepower settings to protect the engine and keep oxygen levels
  without egr in check. Uploading the file from the engine and altering
  the position limiting tables is the easiest solution to this if
  adjustment is necessary. The position limiting is in the
  'Turbo Air Handler Ratio' (TAHR) logic. These tables can be edited to
  adjust the turbocharger positioning...
  
   'C_TAHR_LLim_Table' for the lower limit/min allowed positioning.

   'C_TAHR_ULim_Table' and 'C_TAHR_Prot_ULim_Table' for the upper limit
   /max allowed positioning.
   
		NOTE: These tables are typically adjusted per individual truck
		as the outcome of alterations to egr and exhaust components
		is unpredictable.
		
+ Test equipment well for proper maximum boost levels and adjust as
  necessary. Do not alter the Incal file for this but only the engine
  file taken form the engine directly. If it is desired to make a
  permanent change to the overlay itself for a particular CPL, copy it
  as a different filename and include the CPL in its name. It then can
  be edited directly in Calterm using the 'File-> Open Export File'
  command.

