---
title: 表格Demo
---

```tsx
import React from 'react';
import { GeneratorTable } from 'formily-schema-generator';

export default () => (
  <GeneratorTable
    request={params =>
      Promise.resolve({
        data: [
          {
            array: [
              {
                string: 'Array.0',
                time: '12:00:00',
              },
              {
                string: 'Array.1',
                time: '12:00:00',
              },
            ],
            object: {
              string: 'Object.string',
              textarea: 'Object.textarea',
            },
            string: 'string',
            textarea: 'textarea',
          },
        ],
        success: true,
      })
    }
    schema={[
      {
        type: 'step',
        name: 'step-1',
        title: '步骤',
        description: '步骤组件',
        children: [
          {
            type: 'textarea',
            name: 'textarea',
            title: '多行输入框',
            description: '多行输入框组件',
            key: 'textarea',
          },
          {
            type: 'string',
            name: 'string',
            title: '输入框',
            description: '输入框组件',
            key: 'string',
          },
        ],
        key: 'step',
      },
      {
        type: 'step',
        name: 'step-2',
        title: '步骤',
        description: '步骤组件',
        children: [
          {
            type: 'array',
            name: 'array',
            title: '列表',
            description: '数组组件',
            children: [
              {
                type: 'string',
                name: 'string',
                title: '输入框',
                description: '输入框组件',
                key: 'string_OH4OVK',
              },
              {
                type: 'time',
                name: 'time',
                title: '时间',
                description: '时间',
                key: 'time_OH4OVK',
              },
            ],
            key: 'array',
          },
          {
            type: 'object',
            name: 'object',
            title: '对象',
            description: '对象组件',
            children: [
              {
                type: 'string',
                name: 'string',
                title: '输入框',
                description: '输入框组件',
                key: 'string_a_h9bC',
              },
              {
                type: 'textarea',
                name: 'textarea',
                title: '多行输入框',
                description: '多行输入框组件',
                key: 'textarea_a_h9bC',
              },
            ],
            key: 'object',
          },
        ],
        key: 'step-2',
      },
    ]}
  />
);
```