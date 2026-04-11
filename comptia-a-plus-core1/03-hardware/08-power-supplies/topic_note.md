The [electrical current](https://en.wikipedia.org/wiki/Electric_current) flowing from a standard [wall outlet](https://en.wikipedia.org/wiki/AC_power_plugs_and_sockets) is violent, [oscillating](https://en.wikipedia.org/wiki/Oscillation) back and forth dozens of times a second. If you connected this raw [alternating current](https://en.wikipedia.org/wiki/Alternating_current) directly to the delicate [silicon](https://en.wikipedia.org/wiki/Silicon) of a [microprocessor](https://en.wikipedia.org/wiki/Microprocessor), the chip would vaporize instantly. A [computer power supply unit](https://en.wikipedia.org/wiki/Power_supply_unit_%28computer%29) acts as a sophisticated electrical refinery. By design, a computer power supply unit converts alternating current from a wall outlet into [direct current](https://en.wikipedia.org/wiki/Direct_current) for internal computer components. It takes the chaotic, oscillating energy from the [power grid](https://en.wikipedia.org/wiki/Electrical_grid) and flattens it into the smooth, highly regulated streams of [voltage](https://en.wikipedia.org/wiki/Voltage) necessary to perform complex logical calculations.

![The chaotic, oscillating waveform of alternating current (AC) must be converted into a stable direct current (DC) before reaching delicate computer components.](https://wikipedia.org/wiki/Special:Redirect/file/Types_of_current_by_Zureks.svg)

For an [IT professional](https://en.wikipedia.org/wiki/Information_technology), selecting the right power supply is not merely a matter of finding a plug that fits. It is an exercise in [capacity planning](https://en.wikipedia.org/wiki/Capacity_planning), [thermal management](https://en.wikipedia.org/wiki/Thermal_management_%28electronics%29), and electrical [physics](https://en.wikipedia.org/wiki/Physics).

## The Source: Navigating Input Voltages

Before a power supply can convert [electrical energy](https://en.wikipedia.org/wiki/Electrical_energy), it must successfully receive it from the building's electrical infrastructure. This presents a geographical challenge, as grid power is not globally standardized. 

The standard input voltage for electrical outlets in [North America](https://en.wikipedia.org/wiki/North_America) is 110 to 120 [volts](https://en.wikipedia.org/wiki/Volt) alternating current (VAC). However, if you deploy a [workstation](https://en.wikipedia.org/wiki/Workstation) in [London](https://en.wikipedia.org/wiki/London) or [Tokyo](https://en.wikipedia.org/wiki/Tokyo), the standard input voltage for electrical outlets in [Europe](https://en.wikipedia.org/wiki/Europe) and [Asia](https://en.wikipedia.org/wiki/Asia) is 220 to 240 volts alternating current. 

To accommodate this variance, power supplies are designed with one of two input mechanisms:
*   **Dual-voltage power supply units:** A dual-voltage power supply unit contains a manual [switch](https://en.wikipedia.org/wiki/Switch) to toggle between 115 VAC and 230 VAC input power. As a technician, failing to set this switch correctly before plugging in the machine will either result in a computer that fails to [boot](https://en.wikipedia.org/wiki/Booting), or one that suffers catastrophic electrical damage.
*   **Auto-switching power supply units:** An auto-switching power supply unit automatically detects and adjusts to the incoming AC voltage without a manual switch. These are vastly preferred in modern IT environments because they eliminate the risk of [human error](https://en.wikipedia.org/wiki/Human_error) during international deployments.

## The Output: Direct Current Voltage Rails

Once the alternating current is drawn in, the power supply divides it into specific pathways called "rails." Modern computer components primarily require positive 3.3 volts, positive 5 volts, and positive 12 volts of direct current. Think of these rails as different pipelines of [water pressure](https://en.wikipedia.org/wiki/Fluid_pressure)—some components require heavy, forceful streams to do physical work, while others require gentle, precise trickles to handle logic.

### The Heavy Lifter: +12V
The positive 12-volt rail is the powerhouse of the system. Historically, the positive 12-volt rail on a power supply typically powers components with motors such as [hard disk drives](https://en.wikipedia.org/wiki/Hard_disk_drive) and [cooling fans](https://en.wikipedia.org/wiki/Computer_fan). However, as computational demands have skyrocketed, the 12V rail has taken on an even more critical role: the positive 12-volt rail on a power supply provides the primary power for modern [processors](https://en.wikipedia.org/wiki/Central_processing_unit), as well as the primary power for dedicated graphics cards. 

### The Logic Pipelines: +5V and +3.3V
Components that do not contain moving parts require significantly less voltage. The positive 5-volt rail on a power supply typically powers older storage drives and specific [motherboard](https://en.wikipedia.org/wiki/Motherboard) [logic circuits](https://en.wikipedia.org/wiki/Logic_gate). Meanwhile, the delicate silicon at the heart of the system relies on an even smaller current; the positive 3.3-volt rail on a power supply typically powers integrated motherboard circuits and [system memory](https://en.wikipedia.org/wiki/Random-access_memory).

### Standby and Legacy Rails
Even when a computer appears completely shut down, it is usually still "listening." The positive 5-volt standby voltage circuit provides continuous power to the motherboard even when the computer is turned off. This trickle of energy is what makes modern convenience possible—the positive 5-volt standby voltage allows a computer to wake from [sleep mode](https://en.wikipedia.org/wiki/Sleep_mode) using a [USB](https://en.wikipedia.org/wiki/USB) device or a network signal ([Wake-on-LAN](https://en.wikipedia.org/wiki/Wake-on-LAN)).

Finally, you may encounter the negative 12-volt rail in your documentation. The negative 12-volt rail is a legacy power supply output previously used for older [serial ports](https://en.wikipedia.org/wiki/Serial_port) and specialized [Peripheral Component Interconnect](https://en.wikipedia.org/wiki/Peripheral_Component_Interconnect) (PCI) cards. Modern motherboards rarely utilize it, but it remains in the [ATX specification](https://en.wikipedia.org/wiki/ATX) for [backward compatibility](https://en.wikipedia.org/wiki/Backward_compatibility).

## The Distribution Network: Connectors

Power is useless if it cannot reach its destination. The power supply utilizes highly specific, keyed [connectors](https://en.wikipedia.org/wiki/Electrical_connector) to route the right voltages to the right hardware.

### Motherboard Power
The main motherboard power connector on modern [ATX power supplies](https://en.wikipedia.org/wiki/ATX) features a 24-pin configuration. This massive cable provides the baseline 3.3V, 5V, and 12V power required to run the board. However, you will frequently see this cable split into two pieces at the end. A 20+4 pin main power connector maintains backward compatibility with older motherboards requiring only a 20-pin connection, allowing the extra 4 pins to simply hang to the side unused if necessary.

![A 24-pin main motherboard power connector. The detachable 4-pin section on the right ensures backward compatibility with older 20-pin motherboards.](https://wikipedia.org/wiki/Special:Redirect/file/24-pin_ATX_power_plug_from_a_Seasonic_PSU_20131105.jpg)

### Processor Supplemental Power
As processors evolved, the 24-pin connector could no longer supply enough 12V power to satisfy them. To solve this, a 4-pin ATX12V connector provides dedicated 12-volt power directly to the computer processor. For heavily threaded workstations and [servers](https://en.wikipedia.org/wiki/Server_%28computing%29), this is expanded; an 8-pin EPS12V connector provides supplemental processor power for high-end motherboards and [multi-core processors](https://en.wikipedia.org/wiki/Multi-core_processor).

### Graphics Supplemental Power
Just like processors, dedicated [graphics processing units](https://en.wikipedia.org/wiki/Graphics_processing_unit) (GPUs) quickly outgrew the power the motherboard could provide through the [PCIe](https://en.wikipedia.org/wiki/PCI_Express) slot. A PCIe power connector delivers dedicated supplemental power to dedicated graphics processing units. 
*   Standard PCIe power connectors are available in **6-pin** configurations.
*   Standard PCIe power connectors are available in **8-pin** configurations.
*   To maximize compatibility, a **6+2 pin PCIe connector** adapts to fit either a 6-pin or an 8-pin graphics card power receptacle. 

![Standard 8-pin and 6-pin PCIe power connectors, used to deliver dedicated supplemental power to high-end graphics processing units.](https://wikipedia.org/wiki/Special:Redirect/file/PCI_Express_Power_Supply_Connector-female_PNr%C2%B00438.jpg)

### Storage and Peripherals
For [data storage](https://en.wikipedia.org/wiki/Computer_data_storage), the industry standard has shifted completely to [SATA](https://en.wikipedia.org/wiki/SATA). A SATA power connector is an L-shaped 15-pin cable used to power modern storage drives and [optical drives](https://en.wikipedia.org/wiki/Optical_disc_drive). Because modern drives have complex electrical needs, a SATA power connector supplies 3.3-volt, 5-volt, and 12-volt power to storage devices.

![A 15-pin SATA power connector, which provides 3.3V, 5V, and 12V direct current to modern storage drives.](https://wikipedia.org/wiki/Special:Redirect/file/SATA_power_cable.jpg)

In older machines, or when connecting specialized case accessories, you will encounter the [Molex connector](https://en.wikipedia.org/wiki/Molex_connector). A Molex connector is a 4-pin peripheral power cable used for older [IDE](https://en.wikipedia.org/wiki/Parallel_ATA) hard drives and case fans. Unlike SATA, a Molex power connector supplies only 5-volt and 12-volt power.

## Physical Design: Cable Management and Modularity

A power supply with dozens of cables attached creates a massive physical obstruction inside a [computer chassis](https://en.wikipedia.org/wiki/Computer_case). To address this, manufacturers offer three tiers of physical modularity.

1.  **Non-Modular:** A non-modular power supply unit has all internal power cables permanently attached to the power supply housing. This is cost-effective but creates a chaotic bundle of unused cables that must be stuffed into empty [drive bays](https://en.wikipedia.org/wiki/Drive_bay).
2.  **Semi-Modular:** A semi-modular power supply unit features permanently attached primary motherboard cables (such as the 24-pin and [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) power, which you are guaranteed to need), but allows peripheral computer power cables to be detached. 
3.  **Fully Modular:** A fully modular power supply unit allows the removal of all internal power cables from the power supply housing. 

![A semi-modular power supply (left) allows unused peripheral cables to be detached, reducing internal case clutter compared to a fully hardwired non-modular supply (right).](https://wikipedia.org/wiki/Special:Redirect/file/Modular_vs_non-modular_PSU.JPG)

> **Why does this matter?** Modular power supplies improve computer case [airflow](https://en.wikipedia.org/wiki/Airflow) by allowing the removal of unused power cables. Removing physical obstructions allows cooling fans to push ambient air over heat sinks much more efficiently, prolonging the lifespan of the entire system.

## Sizing and Stability: Wattage and Efficiency

Power supply capacity is measured in [watts](https://en.wikipedia.org/wiki/Watt). To determine what size power supply you need, total required wattage is calculated by summing the maximum power draw of every internal component within the computer. 

However, you should never buy a power supply that perfectly matches your mathematical total. Technicians typically select a power supply wattage rating that exceeds the total component power requirement by 20 to 30 percent. 

Providing excess power supply capacity prevents system instability during peak computational loads. When a CPU and [GPU](https://en.wikipedia.org/wiki/Graphics_processing_unit) simultaneously throttle up to render a video or process a heavy [database](https://en.wikipedia.org/wiki/Database) query, their power draw spikes violently. If the power supply is operating near its absolute maximum limit, this spike will cause [voltage drops](https://en.wikipedia.org/wiki/Voltage_drop), leading to immediate system crashes, [blue screens](https://en.wikipedia.org/wiki/Blue_screen_of_death), or spontaneous [reboots](https://en.wikipedia.org/wiki/Reboot_%28computing%29).

### The 80 PLUS Standard
No power supply is 100% [efficient](https://en.wikipedia.org/wiki/Energy_conversion_efficiency). The [law of conservation of energy](https://en.wikipedia.org/wiki/Conservation_of_energy) dictates that the remaining percentage of power lost during AC to DC conversion in a power supply dissipates as [heat](https://en.wikipedia.org/wiki/Heat). If a computer requires 500 watts of DC power, and the power supply is extremely inefficient, it might pull 750 watts from the wall, wasting 250 watts entirely as heat.

To standardize this, the industry created the [80 PLUS](https://en.wikipedia.org/wiki/80_Plus) certification. The **80 PLUS certification** is an energy efficiency standard for computer power supply units. An 80 PLUS certified power supply operates with at least 80 percent energy efficiency at 20 percent, 50 percent, and 100 percent of the rated load.

![The 80 PLUS certification logo indicates a power supply converts AC to DC with at least 80 percent energy efficiency, significantly reducing excess heat generation.](https://wikipedia.org/wiki/Special:Redirect/file/80_Plus_Standard.svg)

The 80 PLUS certification tiers include Base, Bronze, Silver, Gold, Platinum, and Titanium. A higher 80 PLUS certification tier indicates less electrical energy is wasted as heat during operation. In enterprise environments running hundreds of machines, upgrading to Titanium efficiency saves immense amounts of money not just on electricity, but on the [air conditioning](https://en.wikipedia.org/wiki/Air_conditioning) required to cool the [server room](https://en.wikipedia.org/wiki/Server_room).

## Redundancy for Mission-Critical Operations

In enterprise IT, a hardware failure cannot mean business failure. If the power supply in a critical database server dies, the entire company halts. To mitigate this risk, technicians utilize redundant power supplies.

![A redundant server power supply featuring dual hot-swappable modules. If one module fails, the other seamlessly sustains the system while the dead module is replaced.](https://wikipedia.org/wiki/Special:Redirect/file/PC-Netzteil_(redundant).jpg)

Redundant power supplies consist of two or more individual power modules installed in a single computer system. A redundant power supply configuration allows a server to remain operational if one power supply module fails. The surviving unit instantly shoulders the full electrical load. 

More importantly, redundant power supplies allow technicians to replace a failed power supply module without shutting down the computer system. You can physically walk up to the [server rack](https://en.wikipedia.org/wiki/19-inch_rack), unclip the dead module, slide it out, and slide a fresh one in—all while the server continues processing data uninterrupted. This [hot-swappable](https://en.wikipedia.org/wiki/Hot_swapping) architecture is the bedrock of modern server [reliability](https://en.wikipedia.org/wiki/Reliability_engineering).