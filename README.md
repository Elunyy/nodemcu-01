# Förklaring av Blink-exempelkod

### Denna exempelkod heter **Blink** och har funktionen att få en LED-lampa att lysa i 1 sekund och sedan släckas i 1 sekund, och detta repeteras.

* Setup körs **en** gång vid start av programmet.
Här defineras en inbyggd LED som en output.

```C++
void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
}
```


### Till skillnad från **Setup** funktionen körs **Loop** funktionen flera gånger tills man säger åt den att sluta i koden eller tills man stänger av programmet.
  
* I följande kodrader sätter man på lampan genom att ändra voltage till HIGH, och stänger av den genom att ändra till LOW. Delayen är skriven i millisekunder, därför är en fördröjning på 1000 en sekund. Om man ändrar på dessa värden kan man få andra längder på blinkningarna.

```
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000);
}
```

* _I det här exemplet finns det ingen kodbit som kan få LED-lampan att sluta blinka, men man hade kunnat sätta in ett värde att kolla efter, exempelvis att den ska sluta lysa efter 10 blinkningar._
