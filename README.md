// Include Libraries
#include "Arduino.h"
#include "Relay.h"
#include "SolenoidLock.h"


// Pin Definitions
#define FINGERPRINTSCANNER_5V_PIN_RX	10
#define FINGERPRINTSCANNER_5V_PIN_TX	11
#define RELAYMODULE_PIN_SIGNAL	3
#define SOLENOIDLOCK_PIN_GND	2



// Global variables and defines

// object initialization
Relay relayModule(RELAYMODULE_PIN_SIGNAL);
SolenoidLock solenoidLock(SOLENOIDLOCK_PIN_GND);


// define vars for testing menu
const int timeout = 10000;       //define timeout of 10 sec
char menuOption = 0;
long time0;

// Setup the essentials for your circuit to work. It runs first every time your circuit is powered with electricity.
void setup() 
{
    // Setup Serial which is useful for debugging
