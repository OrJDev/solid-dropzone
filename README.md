# Solid DropZone

SolidJS Adapter For React DropZone

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
