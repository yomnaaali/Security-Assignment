# Steganography Tool

## 📌 Overview
This project is a **Windows Forms Application** built with **C#** that implements **Steganography** to hide and extract text from images.

## 🚀 Features
- **Load an Image**: Select an image to use for text hiding.
- **Hide Text in Image**: Embed a secret message into the image with minimal visual distortion.
- **Extract Hidden Text**: Retrieve the hidden message from a steganographic image.

## 🛠️ How It Works
### 🔹 Hiding Text (`HideText` Method)
1. Converts the text message into binary.
2. Appends a null terminator (`00000000`) at the end to signal the stopping point.
3. Modifies the least significant 2 bits of each **R, G, and B** color channel to store the binary data.
4. Saves the modified image with the hidden text.

### 🔹 Extracting Text (`ExtractText` Method)
1. Reads the least significant 2 bits from the **R, G, and B** channels for each pixel.
2. Reconstructs the binary string and converts it back into text.
3. Stops extracting when the null terminator (`00000000`) is found.

## 📂 Project Structure
```
📦 Steganography
 ┣ 📂 steganography (Main Project Folder)
 ┃ ┣ 📜 Program.cs (Main Entry Point)
 ┃ ┣ 📜 Form1.cs (UI Logic & Event Handling)
 ┃ ┣ 📂 Helpers
 ┃ ┃ ┣ 📜 Steganography.cs (Hiding & Extracting Logic)
 ┣ 📜 steganography.sln (Visual Studio Solution File)
```

## 🎯 Usage
1. **Run the application** in Visual Studio.
2. **Load an image** by selecting it from your system.
3. **Enter a secret message** and hide it inside the image.
4. **Save the modified image** containing the hidden text.
5. **Extract the message** later by loading the steganographic image.

## 📌 Technologies Used
- **C#** (Windows Forms)
- **Bitmap Processing** for pixel manipulation

## 📜 License
This project is open-source and available for use under the MIT License.

