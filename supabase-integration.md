# Supabase Integration Guide

## Introduction
This guide will help you integrate Supabase with your website.

## Setting Up the Supabase Client
1. **Install Supabase**: If using npm, run:
   ```bash
   npm install @supabase/supabase-js
   ```

2. **Initialize Supabase**:
   ```javascript
   import { createClient } from '@supabase/supabase-js';

   const supabaseUrl = 'https://lsavwgxllooikpxnvwiv.supabase.co';
   const supabaseAnonKey = 'YOUR_ANON_KEY'; // Replace with your anon key
   const supabase = createClient(supabaseUrl, supabaseAnonKey);
   ```

## Connecting to Your Project
- Replace `YOUR_ANON_KEY` with the anon key found in your Supabase project settings.

## Code Examples

### Authentication
- **Sign Up**:
   ```javascript
   const { user, session, error } = await supabase.auth.signUp({
     email: 'user@example.com',
     password: 'securepassword',
   });
   ```

- **Sign In**:
   ```javascript
   const { user, session, error } = await supabase.auth.signIn({
     email: 'user@example.com',
     password: 'securepassword',
   });
   ```

- **Sign Out**:
   ```javascript
   const { error } = await supabase.auth.signOut();
   ```

### Database Operations
- **Insert Data**:
   ```javascript
   const { data, error } = await supabase
     .from('your_table_name')
     .insert([{
       column1: 'value1',
       column2: 'value2',
     }]);
   ```

- **Select Data**:
   ```javascript
   const { data, error } = await supabase
     .from('your_table_name')
     .select('*');
   ```

- **Update Data**:
   ```javascript
   const { data, error } = await supabase
     .from('your_table_name')
     .update({ column1: 'new_value' })
     .match({ id: 1 });
   ```

- **Delete Data**:
   ```javascript
   const { data, error } = await supabase
     .from('your_table_name')
     .delete()
     .match({ id: 1 });
   ```

## Conclusion
Integrating Supabase provides you with powerful backend capabilities and real-time functionality to your website.