---
title: Función DateFromParts (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Devuelve un valor de fecha para el año, el mes y el día especificados.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423226"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Función DateFromParts (aplicación web personalizada de Access)

Devuelve un valor de fecha para el año, el mes y el día especificados.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**DateFromParts** (*Year*, *Month*, *Day*) 
  
La **función DateFromParts** contiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Year*  <br/> |Expresión entera que especifica un año.  <br/> |
| *Month*  <br/> |Expresión entera que especifica un mes, de 1 a 12.  <br/> |
| *Day*  <br/> |Expresión de entero que especifica un día.  <br/> |
   
## <a name="remarks"></a>Comentarios

**DateFromParts** devuelve un valor de fecha con la parte de fecha establecida en el año, mes y día especificados, y la parte de hora establecida en el valor predeterminado. Si los argumentos no son válidos, se genera un error. Si los argumentos necesarios son nulos, se devuelve NULL. 
  
## <a name="example"></a>Ejemplo

La expresión siguiente usa la **función DateFromParts** para calcular el primer día del mes actual. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



