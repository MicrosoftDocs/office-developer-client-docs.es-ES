---
title: Función Try_Parse (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analiza un valor de texto en el tipo de datos especificado en la referencia cultural de la aplicación o devuelve NULL si la conversión no es válida.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307801"
---
# <a name="tryparse-function-access-custom-web-app"></a>Función Try_Parse (aplicación web personalizada de Access)

Analiza un valor de texto en el tipo de datos especificado en la referencia cultural de la aplicación o devuelve NULL si la conversión no es válida.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Try_Parse** (*TextExpression*, *DataType*) 
  
La función **Try_Parse** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *TextExpression*  <br/> |Una expresión de texto que representa el valor con formato que se va a analizar en el tipo de datos especificado.  <br/> |
| *DataType*  <br/> |El tipo de datos en el que se va a analizar *TextExpression* .  <br/> |
   
## <a name="remarks"></a>Comentarios

Use **Try_Parse** solo para convertir de cadena en tipos de número, fecha y hora. Para las conversiones de tipo generales, continúe usando **Convert**. 
  

