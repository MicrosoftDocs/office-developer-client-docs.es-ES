---
title: Parse (función) (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analiza un valor de texto y devuelve su valor en un tipo dado utilizando la referencia cultural de la aplicación.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815470"
---
# <a name="parse-function-access-custom-web-app"></a>Parse (función) (aplicación web personalizado de Access)

Analiza un valor de texto y devuelve su valor en un tipo dado utilizando la referencia cultural de la aplicación.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Analizar** (*TextExpression*, *tipo de datos*) 
  
La función **analizar** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *TextExpression*  <br/> |Una expresión de texto que representa el valor con formato para analizar en el tipo de datos especificado.  <br/> |
| *DataType*  <br/> |Valor literal que representa el tipo de datos solicitado para el resultado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Use **analizar** sólo para convertir una cadena de fecha y hora y tipos de número. Para las conversiones de tipo general, use la función **convertir** . Tenga en cuenta que hay un cierto nivel de performance una sobrecarga en el valor de cadena de análisis. 
  

