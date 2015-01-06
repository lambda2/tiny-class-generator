TIny CLAss GEnerator
====================

A tiny cpp class bootstraper

## Usage
`ticlage [className] [[attribute:type]...]`

ex: `$> ticlage boat length:int name:std::string` will generate Boat.cpp and Boat.h like:
```c++
// Boat.cpp
#include "Boat.h"
Boat::Boat()
{

}

Boat::~Boat()
{

}

void Boat::set_length(int value)
{
	this->length = value;
}

int Boat::get_length(void) const
{
	return (this->length);
}

void Boat::set_name(std::string value)
{
	this->name = value;
}

std::string Boat::get_name(void) const
{
	return (this->name);
}
```

```c++
// Boat.h
#ifndef BOAT_H
#define BOAT_H

class Boat
{

public:
	Boat();
	~Boat();

	void set_length(int value);
	int get_length(void) const;
	void set_name(std::string value);
	std::string get_name(void) const;
	
private:
	int length;
	std::string name;
};

#endif
```
