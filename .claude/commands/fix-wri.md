# Fix WRI Compliance Issues

Automatically fix common WRI Design System compliance issues in the current file:

1. **Fix Hardcoded Colors**
   - Find all hardcoded hex/rgb color values
   - Determine the closest WRI color token match
   - Replace with `getThemedColor(palette, shade)`
   - Add import if needed

2. **Fix Modal Props**
   - Replace `isOpen` with `open`
   - Replace `children` with `content`
   - Update JSX structure if needed

3. **Fix Select Props**
   - Replace `options` with `items`
   - Replace `value` with `defaultValue`
   - Fix onChange handler signature

4. **Fix RadioGroup**
   - Add `name` prop if missing
   - Fix onChange signature

5. **Add Missing Imports**
   - Ensure `getThemedColor` is imported if used
   - Ensure `designSystemStyles` is imported if ChakraProvider is used

After fixing, run validation to confirm all issues are resolved.
