---
title: Sección Archivo de configuración de formulario [Verbos]
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
# <a name="form-configuration-file-verbs-section"></a>Sección Archivo de configuración de formulario [Verbos]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **sección [Verbos]** enumera el conjunto completo de verbos admitidos por el formulario. El formato de la **sección [Verbos]** es: 
  
 **[Verbos]**
  
 **Verb1**  =   _string_
  
A continuación se muestra un ejemplo de **una sección [Verbos].** 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Cada verbo se define en un **[Verbo] independiente.** _string_ **]** section. A **[Verb.** _string_ **]** section describe un verbo único ofrecido por el formulario. La **entrada DisplayName** en **un [Verb.** _string_ **]** section especifica el nombre del comando que se muestra en la interfaz de usuario. La **entrada Code** corresponde al número de verbo pasado en el método [IMAPIForm::D oVerb.](imapiform-doverb.md) Sintaxis de **[Verb.** _string_ **]** section es: 
  
 **[Verbo.** _string_ **]**
  
 **DisplayName**  =   _cadena mostrada_
  
 **Código**  =   _entero_
  
 **Marcas**  =   _entero_
  
 **Attribs**  =   _entero_
  
A continuación se muestra un ejemplo **de un [Verb.** _string_ **]** section. 
  
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

Los verbos enumerados en esta sección los recupera un cliente mediante el [método IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md). Los verbos se activan llamando al método [IMAPIForm::D oVerb](imapiform-doverb.md) del formulario y pasando el número de código del verbo que se va a realizar. 
  

