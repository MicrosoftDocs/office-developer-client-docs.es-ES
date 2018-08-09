---
title: Función DateDiff (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Devuelve el recuento de los límites de parte de fecha especificada cruzado entre la fecha de inicio especificada y la fecha de finalización.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815346"
---
# <a name="datediff-function-access-custom-web-app"></a>Función DateDiff (aplicación web personalizado de Access)

Devuelve el recuento de los límites de parte de fecha especificada cruzado entre la fecha de inicio especificada y la fecha de finalización.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
La función **DateDiff** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *DatePart*  <br/> |Es la parte de *StartDate* y *EndDate* que especifica el tipo de límite cruzado. Consulte la sección Comentarios para obtener una lista de configuraciones válidas.  <br/> |
| *StartDate*  <br/> |Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  <br/> |
| *EndDate*  <br/> |Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  <br/> |
   
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
   

