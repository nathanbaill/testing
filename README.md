# Testing

Saint Michel Annecy, IT Campus, testing for L3 CSI and Master MS2D.
It covers many aspects of modern software testing, from unit tests to, integration test, embedded development testing, etc

## Testing using Pytest

Pytest means Python, it's a framework to test Python using Python.
First create a virtual environment.

```bash
python3 -m venv venv
```

Then activate it.

```bash
source venv/bin/activate
```

Then install pytest and other dependencies of that project.

```bash
pip install -r requirements.txt
```

Running the tests.

```bash
pytest
```

## Embedded development testing

A piece of code can test another piece of code from the same project.
But testing can be performed through a more abstract protocol, radio, serial, etc
The goal of those tests is to discover a very cheap microcontroller, the ATMega328P,
and its development environment, the Arduino one.
It highlights the differences between the Arduino framework and its simple MCU
and our modern desktop environment looking at various aspects such as arithmetic precision
and memory management.

### Arduino

Development will be made under VSCode using Arduino plugin to access copilot 
to easily develop the embedded software and Arduino IDE to have the full
options of the Arduino environment. See the [IDE installation procedure on the Arduino website](https://support.arduino.cc/hc/en-us/articles/360019833020-Download-and-install-Arduino-IDE).

Open the `arduino/arduino.ino` file with Arduino IDE and upload it to the board.
At the point the test `test_arduino.py` should pass.