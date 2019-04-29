---
title: Función DateAdd (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Devuelve una fecha especificada con el intervalo especificado de número (entero positivo o negativo) que se agrega a una parte de fecha especificada de la fecha.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423205"
---
# <a name="dateadd-function-access-custom-web-app"></a>Función DateAdd (aplicación web personalizada de Access)

Devuelve una fecha especificada con el intervalo especificado de número (entero positivo o negativo) que se agrega a una parte de fecha especificada de la fecha.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**DateAdd** (*DatePart*, *Number*, *Date*) 
  
La función **DateAdd** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *DatePart*  <br/> |La parte de la  *Fecha*  a la que se agrega un entero. Consulte la sección Comentarios para obtener una lista de configuraciones válidas.  <br/> |
| *Número*  <br/> |Es una expresión que se puede resolver en un entero que se agrega a  *ParcFecha*  de  *Fecha*  . Si especifica un valor con una fracción decimal, la fracción se trunca.  <br/> |
| *Fecha*  <br/> |Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  <br/> |
   
## <a name="remarks"></a>Comentarios

La siguiente tabla muestra todos los argumentos  *ParcFecha*  válidos. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**quarter** <br/> |
|**month** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**week** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**millisecond** <br/> |
   
## <a name="example"></a>Ejemplo

La siguiente expresión calcula el último día del mes actual.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

La siguiente expresión calcula el último día del mes anterior.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


