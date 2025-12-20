# RED

## Category 🕵️: Forensics
## Difficulty 🟢: Easy
## Solves as of: December 20, 2025 — <img width="1289" height="625" alt="image" src="https://github.com/user-attachments/assets/5f5427fa-a970-4023-afcc-14bdb8b350df" />

    Caption: This challenge has been solved by 21,355 players, indicating it is a popular challenge that many players were able to complete.

## Guide Published 📝: December 20, 2025

## Challenge Summary 🧩
A seemingly plain red image hides data that isn’t visible to the eye; this task reinforces looking beyond pixels by inspecting color channels and file internals. You’ll practice detecting and extracting concealed content with [`"zsteg"`](https://linuxcommandlibrary.com/man/zsteg#:~:text=zsteg%20is%20a%20command%2Dline,methods%20involving%20zlib%20compressed%20streams.) and then translating a hidden blob via [`"Base64"`](https://builtin.com/software-engineering-perspectives/base64-encoding) decoding to reveal the flag.

---

## Key Objective 🎯
Extract concealed data from a red [`"PNG"`](https://www.adobe.com/creativecloud/file-types/image/raster/png-file.html) by scanning for steganographic payloads with `"zsteg"` and decoding the discovered `"Base64"` string.

---

## Prerequisites & Tools 🔧
- `"PNG"` basics (containers, chunks)  
- Understanding of [`"RGB"`](https://en.wikipedia.org/wiki/RGB_color_model) color channels and how data can be hidden in them  
- Knowing what [`"metadata"`](https://www.techtarget.com/whatis/definition/metadata) is and where it lives in image files  
- Tools: `"zsteg"`, [`"exiftool"`](https://www.youtube.com/watch?v=JMw6mXFKbm8), a reliable `"Base64"` decoder (e.g., [`"Base64 Encoder/Decoder"`](https://www.base64decode.org/))

---

## Walkthrough 🚀 (with WHY)
1) Download the challenge file `red.png`.  
   **WHY:** You need the local artifact to inspect its internals and run `"zsteg"` analysis.

<img width="1418" height="335" alt="image" src="https://github.com/user-attachments/assets/e8cebd6e-7aad-4a8b-b722-0683da8ec77b" />
  
    Caption: Local copy of the challenge image saved as red.png for analysis.

2) Run `"zsteg"` on the `"PNG"` to scan common steganography patterns (including bit-plane encodings in color channels).  
   **WHY:** `"zsteg"` rapidly tests many hiding schemes (like least significant bits) so you don’t have to guess where payloads live.

  <img width="2365" height="310" alt="image" src="https://github.com/user-attachments/assets/2fbc3412-5b42-4084-98b9-d64f48c02015" />

     Caption: `"zsteg"` output showing a suspicious line that includes Base64-like characters.

3) Identify the line that looks like `"Base64"` (letters, digits, `+`, `/`, and possibly `=` at the end).  
   **WHY:** A `"Base64"` blob is a strong indicator of embedded text or another layer of data that must be decoded next.

  <img width="2414" height="300" alt="image" src="https://github.com/user-attachments/assets/9f0572a2-89db-4668-8913-e6f4aa18dcc7" />
  
     Caption: Extracted Base64 string copied from `"zsteg"` results for decoding.

4) Paste the blob into a trusted `"Base64"` decoder and decode it.  
   **WHY:** Decoding translates the encoded payload into readable text, which yields the flag.

  <img width="1228" height="858" alt="Screenshot 2025-10-10 113201" src="https://github.com/user-attachments/assets/c9b08cf8-1717-4a02-84a0-10f485d6eb6a" />

      Caption: Decoded output from the Base64 string revealing the hidden message.

5) (Optional) Check `"metadata"` with `"exiftool"`.  
   **WHY:** While not necessary here, quick `"metadata"` checks help confirm whether clues are stored in tags instead of pixels.

  <img width="2129" height="474" alt="image" src="https://github.com/user-attachments/assets/0530aed8-d38a-4ed6-a3dd-32b0eaf95369" />
 
      Caption: `"exiftool"` report confirming no useful metadata for this solve.

---

## Common Mistakes ⚠️
- Relying on `"strings"` repeatedly when steganography often hides data in bit-planes, which `"strings"` won’t expose efficiently.  
- Using `"binwalk -e"` expecting embedded files, even though the payload is an inline bit-level encoding rather than a packed file.  
- Grepping hex dumps with `"xxd"` after you already have a clear `"Base64"` lead.

---

## Lessons Learned ✅
- Steganography challenges benefit from targeted tools like `"zsteg"` because they automate checks across many hide-in-color-channel patterns.  
- Recognizing `"Base64"` patterns accelerates extraction, turning opaque blobs into readable content quickly and reliably.
