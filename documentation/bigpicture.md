---
layout: page
title: The big picture
---

![](bigpicture.png)

Original graph source:

    style=filled;
    color=lightgrey;
    node [shape=box, color=purple ];
    rankdir=LR;
    resolution = "75";


    subgraph cluster_0 {
        style=filled;
        color=lightgrey;
        node [style=filled,color=white];
        "FusionInventory for GLPI" -> "GLPI engine" -> "DB";
        label = "GLPI";
    }

    subgraph cluster_1 {

        subgraph cluster_4 {

            color=gainsboro;
            "Local Inventory" -> "Agent" -> "FusionInventory for GLPI";
            "ESX Inventory" -> "Agent";
            "Network Inventory" -> "Agent";
            "Agent" -> "Deploy";
            label = "FusionInventory Agent";
        }

        style=filled;
        color=lightgrey;
        node [style=filled,color=white];
        "dmidecode" -> "Local Inventory";
        "dpkg" -> "Local Inventory";
        "registry" -> "Local Inventory";
        "rpm" -> "Local Inventory";
        "WMI" -> "Local Inventory";
        "dmidecode" -> "Local Inventory";
        "PCI info" -> "Local Inventory";
        "USB info" -> "Local Inventory";
        "virtual machines" -> "Local Inventory";
        "more" -> "Local Inventory";
        "Deploy" -> "set some configuration";
        "Deploy" -> "add software";
        label = "Computer(s)";
    }

    subgraph cluster_2 {
        style=filled;
        color=lightgrey;
        node [style=filled,color=white];
        "vCenter1" -> "ESX Inventory";
        "esx4" -> "ESX Inventory";

        "esx1" -> "vCenter1";
        "esx2" -> "vCenter1";
        "esx3" -> "vCenter1";
        "vm1" -> "esx1";
        "vm2" -> "esx2";
        "vm3" -> "esx2";
        "vm4" -> "esx3";
        "vm5" -> "esx3";
        "vm6" -> "esx4";
        label = "VMware API";
    }

    subgraph cluster_3 {
        style=filled;
        color=lightgrey;
        node [style=filled,color=white];
        "printer 1" -> "Network Inventory";
        "printer 2" -> "Network Inventory";
        "switch 1" -> "Network Inventory";
        "unknown device" -> "Network Inventory";
        label = "Networks";
    }

