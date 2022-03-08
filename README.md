# georgian-phone-number-regex
Gor now this is only for GSM checks  [Example Online](https://regex101.com/r/Z5ePey/1)
```regex
^(\+\d{3}\s?)?\(?\d{3}\)?[\s.-]?\d{3}[\s.-]?\d{3}$
```
Valid inputs:
- 123-456-789  
- (123) 456-789  
- 123 456 789  
- 123.456.789  
- +995 568 000 865
- +995568000865
- 568 000 000  
- 568000000  

Validation code sample:  
```typescript
export const validatePhoneNumber = (phone: string):boolean => {
  return phone.match(/^(\+\d{3}\s?)?\(?\d{3}\)?[\s.-]?\d{3}[\s.-]?\d{3}$/);
};
```
