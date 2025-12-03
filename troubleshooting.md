# Troubleshooting Notes

## Hyper-V Ubuntu VM Issues

### PXE Boot Error
**Symptom:** VM tries to boot from network (PXE) instead of ISO.  
**Fix:** Change boot order to prioritize DVD drive first.

---

### Secure Boot Block
**Symptom:** Ubuntu installer fails to start under Hyper-V Secure Boot.  
**Fix:** Disable Secure Boot in VM settings to allow unsigned Linux ISOs.
