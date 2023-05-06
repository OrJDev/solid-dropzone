# Solid DropZone

SolidJS Adapter For React DropZone

### Info

I was working on a SolidJS adapter for UploadThing, noticed it was using React DropZone so I was looking for a SolidJS DropZone adapter and faced an issue with the existing one where it was not working and threw an error (attr-etc is not installed), so i copied the code of it and made a few changes to make it work + used my own build config. The repo [is here](https://github.com/soorria/solid-dropzone) so thanks to the original author.

## Install

```sh
pnpm install solidjs-dropzone
```

## Usage

```tsx
import { useDropzone } from "solidjs-dropzone";

function MyDropzone() {
  const onDrop = (acceptedFiles: File[]) => {
    // Do something with the files
  };
  const { getInputProps, getRootProps, isDragActive } = useDropzone({ onDrop });
  return (
    <div {...getRootProps()}>
      <input {...getInputProps()} />
      {dropzone.isDragActive ? (
        <p>Drop the files here ...</p>
      ) : (
        <p>Drag 'n' drop some files here, or click to select files</p>
      )}
    </div>
  );
}
```
