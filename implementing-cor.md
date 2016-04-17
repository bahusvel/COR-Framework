# Implementing COR-Framework
COR-Framework encourages you to implement it in any runtime possible, whether its a different programming language or different platform. This document will guide you through the process of implementing COR-Framework on your own.
Typically COR-Framework implementation consists of several major components:
* Module API
* Networking
* Loader

## Module API
Module API is responsible for communicating with the modules developed for COR-Framework, it MUST provide the following endpoints/methods for the module:
* message_out(message) to send messages from the module to the COR-Network
* add_topic(message_type, message_callback) to declare endpoints within the module that will be called when messages of declared types are received
* add_type(message_type, message_instance_callback) to declare the supported message types along with the corresponding implementations

## Networking

## Messages

## Loader

## Reference Implementation
COR-Framework-Python is the most current implementation of COR-Framework available, features implemented there are considered to be fully approved and supported by COR-Framework, if you are implementing COR-Framework in your runtime and would like to test it, please use COR-Framework-Python as the reference: https://github.com/bahusvel/COR-Framework-Python.git


