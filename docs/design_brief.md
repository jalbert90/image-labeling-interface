# Problem Statement

An invoice line-item extraction pipeline that uses **Optical Character Recognition** (**OCR**) to extract text and a **Layout Language Model** (**LayoutLM**) to classify it requires the LayoutLM to be fine-tuned on labeled OCR data. The OCR output data is in JSON format and includes the extracted texts and their corresponding bounding boxes. Each bounding box must then be given a label, a tedious, error-prone, and time-consuming process that involves manually editing JSON files.

# Solution

A visual and intuitive, browser-based labeling interface that eliminates the need for manually editing JSON files. The interface consists of a main viewing window where images are shown with overlain bounding boxes. Each bounding box can then be clicked, edited, and labeled quickly.

# Target Users

1. **Primary:** Anyone who needs to label OCR data for LayoutLM training.
2. **Secondary:** Anyone who needs to review/edit image annotations.

# Key Features (tentative)

- Users can upload invoice images and their corresponding annotations (the OCR data).
- The system will attempt to automatically match each invoice image with its annotation JSON file.
- Matches can be made manually if need be.
- Once an invoice is matched with its annotation data, it is shown with overlain bounding boxes.
- Bounding boxes can be selected, resized, labeled, and have their text contents changed.
- All changes are stored in the browser.
- Annotations can then be exported as new JSON files, leaving the original JSON files intact.
- A working area on the right provides a list of bounding boxes, their text contents, and labels.