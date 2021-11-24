# Form Builder Application

Contributions and Pull Requests's are welcome! This is a project we started to help friends who are volunteering and collecting on paper form data but getting exhausted entering data to a database. If you have experience with web dev, image recognition / Optical Character Recognition (OCR), or want to learn about these you can contact us to contribute!

We would like to prepare forms online by drag & drop, print them on paper and scan them with our phones to take results back.

### Problem our friends faced

Smartphones are not available in disadvantaged communities to ask people to fill out online forms, so we are exploring alternatives.

## Service Architecture (WIP)

The backend consists of multiple microservices:

![cloud diagram](./diagrams/arch.png)

1. Image Manipulator (Lambda)

Image manipulator is responsible for handling images that are uploaded to the service. Handling includes:

- Resizing, flattening
- OCR (optical character recognition)
- Extract data associated with each part, call CRUD layer with the extracted data.

2. CRUD layer (Express server with Lambda)

Gets form id, and its components along with the data. Saves them to database.

## Web App

Create forms with drag & drop UI, share them as online forms with a link.

- Print forms to be distributed in paper.
- Can also fill out forms online.
