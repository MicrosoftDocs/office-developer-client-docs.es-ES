---
title: Función Try_Parse (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analiza un valor de texto para el tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815510"
---
# <a name="tryparse-function-access-custom-web-app"></a>Función Try_Parse (aplicación web personalizado de Access)

Analiza un valor de texto para el tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Try_Parse** (*TextExpression*, *tipo de datos*) 
  
La función **Try_Parse** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *TextExpression*  <br/> |Una expresión de texto que representa el valor con formato para analizar en el tipo de datos especificado.  <br/> |
| *DataType*  <br/> |El tipo de datos en el que se va a analizar *TextExpression* .  <br/> |
   
## <a name="remarks"></a>Comentarios

Use **Try_Parse** sólo para convertir una cadena de fecha y hora y tipos de número. Para las conversiones de tipo general, seguir usando **convertir**. 
  

