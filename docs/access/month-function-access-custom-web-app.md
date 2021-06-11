---
title: Función Month (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Devuelve un entero que representa el mes de la fecha especificada.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411494"
---
# <a name="month-function-access-custom-web-app"></a>Función Month (aplicación web personalizada de Access)

Devuelve un entero que representa el mes de la fecha especificada.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Month** (*Date*) 
  
La **función Month** contiene el argumento siguiente. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Date*  <br/> |Una expresión que se puede resolver en un valor Fecha/Hora.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **Month** devuelve el mismo valor que **DatePart** (mes, fecha). 
  
Si  *Date*  solo contiene una parte de tiempo, el valor devuelto es 1, el mes base. 
  

