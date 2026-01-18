#define DEVICE 8   // Relay or LED connected to pin D8

void setup() {
  pinMode(DEVICE, OUTPUT);
  digitalWrite(DEVICE, LOW);   // Device OFF initially

  Serial.begin(9600);
  Serial.println("Speech Recognition System Ready");
  Serial.println("Type ON or OFF and press Enter");
}

void loop() {
  if (Serial.available() > 0) {
    String command = Serial.readStringUntil('\n');
    command.trim();  // Remove spaces and new line

    if (command == "ON") {
      digitalWrite(DEVICE, HIGH);
      Serial.println("Device ON");
    }
    else if (command == "OFF") {
      digitalWrite(DEVICE, LOW);
      Serial.println("Device OFF");
    }
    else {
      Serial.println("Invalid Command");
    }
  }
}
