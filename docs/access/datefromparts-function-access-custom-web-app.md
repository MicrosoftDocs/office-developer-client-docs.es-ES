---
title: Función DateFromParts (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Devuelve un valor de fecha para el año especificado, el mes y el día.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815294"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Función DateFromParts (aplicación web personalizado de Access)

Devuelve un valor de fecha para el año especificado, el mes y el día.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**DateFromParts** (*Año*, *mes*, *día*) 
  
La función **DateFromParts** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *year*  <br/> |Expresión de tipo entero que especifica un año.  <br/> |
| *Month*  <br/> |Expresión de tipo entero que especifica un mes, de 1 a 12.  <br/> |
| *Día*  <br/> |Expresión de tipo entero que especifica un día.  <br/> |
   
## <a name="remarks"></a>Comentarios

**DateFromParts** devuelve un valor de fecha con la parte de fecha establecida en la parte de la hora establecida en el valor predeterminado, mes y día y el año especificado. Si los argumentos no son válidos, se produce un error. Si es necesario argumentos son nulos, se devuelve NULL. 
  
## <a name="example"></a>Ejemplo

La siguiente expresión usa la función **DateFromParts** para calcular el primer día del mes actual. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



