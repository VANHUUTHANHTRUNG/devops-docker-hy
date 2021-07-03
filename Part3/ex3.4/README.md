# Step #
- For frontend: remove apt, reinstall ca-certificates, remove everything in 
`/usr/src/app` except `build` directory
- For backend: remove apt, remove everything in `/usr/src/app` except `server`

# Result #
- App runs as expected
- fontend image was reduced from 1170104175 Byte to 988927445 Byte
- backend image remains the same size at 1007990780 Byte

**Removing file without changing base image or multi-stage building seems not as 
good as I expected. Still no idea why the backend image remains the same
