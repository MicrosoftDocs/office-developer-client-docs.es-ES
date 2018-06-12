---
title: Función DateAdd (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Devuelve una fecha especificada con el intervalo especificado de número (entero positivo o negativo) que se agrega a una parte de fecha especificada de la fecha.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815348"
---
# <a name="dateadd-function-access-custom-web-app"></a>Función DateAdd (aplicación web personalizado de Access)

Devuelve una fecha especificada con el intervalo especificado de número (entero positivo o negativo) que se agrega a una parte de fecha especificada de la fecha.
  
> [!NOTE]
> [!NOTA] La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateAdd** (*DatePart*, *número*, *fecha*) 
  
La función **AgregFecha** contiene los siguientes argumentos. 
  
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


