## How Antivirus Scan ?	
 1. Signatures-based detection:
  - Looks for the specific digital code.

 2. Heuristics-based detection:
  - Looks for specific instructions using a rule or weight-based system.

 3. Behavior-based detection:
  - Looks for software attempting to perform malicious functions.
 
 4. Machine learning:
  - Analyze the code of applications and decide based on its understanding of malicious and benign programs.

## Cryptographic Hashing:
 - MD5: 128 bits
 - SHA-1: 160 bits
 - SHA-256: 256 bits

## Portable Executable (PE) File Formate:
 - The PE file formate is a data structure that constains the information necessary fot the Windows OS loader to manage the executable code.
 - e.g.: .exe/ .dll/ .sys/ .fon/ .drv

### Basic Structure of PE files:
 1. DOZ MZ header:
  - 64 bytes, Its signature 'MZ' `4D 5A`.
 2. DOS stub:
  - Only prints out the message "This program cannot be run in DOS mode" when the image is run in MS-DOS.
 3. PE header:
  - Signature: 4 bytes 'PE' `50 45 00 00`.
  - File Header: 20 bytes after signature contains number of sections, TimeDateStamp and Characteristics. 
  - Optional header: Comes after File Header and It conatains:
   - `AddressOFEntryPoint`: Virtual address where the EXE file wll first begin execution.
   - Preferred Load Image `ImageBase`: Important in dynamic analysis.
   - `SizeOfImage`: The overall size of image.  
 4. Section:
 - the first three headers are important in static analysis, the section header is important in dynamic analysis.