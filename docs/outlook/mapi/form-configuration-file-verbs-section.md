---
title: Sección del archivo de configuración de formulario [verbos]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417787"
---
# <a name="form-configuration-file-verbs-section"></a>Sección del archivo de configuración de formulario [verbos]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[verbs]** muestra el conjunto completo de verbos admitidos por el formulario. El formato de la sección **[verbs]** es: 
  
 **Verbos**
  
 **** =  _Cadena_ Verb1
  
A continuación se encuentra un ejemplo de una sección **[verbs]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Cada verbo se define en un **[verbo.** _cadena_ de **]** sección. **[Verbo.** _cadena_ de **]** describe un único Verbo ofrecido por el formulario. La entrada **displayName** en **[Verb.** _cadena_ de **]** especifica el nombre de comando que se muestra en la interfaz de usuario. La entrada de **código** corresponde al número de verbo pasado en el método [IMAPIForm::D overb](imapiform-doverb.md) . La sintaxis del **verbo.** _cadena_ de **]** es: 
  
 **Verbo.** _cadena_ de **]**
  
 **** =  _Cadena mostrada_ como DisplayName
  
 **** =  _Número entero_ del código
  
 **Indicadores** =  _enteros_
  
 **** =  _Entero_ attribs
  
A continuación se encuentra un ejemplo de **[Verb.** _cadena_ de **]** sección. 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

Los verbos que se enumeran en esta sección los recupera un cliente mediante el [método IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md). Los verbos se activan llamando al método [IMAPIForm::D overb](imapiform-doverb.md) del formulario y pasándole el número de código del verbo que se va a realizar. 
  

