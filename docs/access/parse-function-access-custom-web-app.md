---
title: Función Parse (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analiza un valor de texto y devuelve su valor en un tipo determinado mediante la referencia cultural de la aplicación.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411137"
---
# <a name="parse-function-access-custom-web-app"></a>Función Parse (aplicación web personalizada de Access)

Analiza un valor de texto y devuelve su valor en un tipo determinado mediante la referencia cultural de la aplicación.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Parse** (*TextExpression*, *DataType*) 
  
La **función Parse** contiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *TextExpression*  <br/> |Expresión de texto que representa el valor con formato que se debe analizar en el tipo de datos especificado.  <br/> |
| *DataType*  <br/> |Valor literal que representa el tipo de datos solicitado para el resultado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Use **El análisis solo** para convertir de cadena a tipos de fecha y hora y números. Para conversiones de tipos generales, use la **función** Convert. Tenga en cuenta que hay una sobrecarga de rendimiento determinada al analizar el valor de la cadena. 
  

