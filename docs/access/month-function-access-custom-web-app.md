---
title: Función Month (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Devuelve un valor de tipo integer que representa el mes de la fecha especificada.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815467"
---
# <a name="month-function-access-custom-web-app"></a>Función Month (aplicación web personalizado de Access)

Devuelve un valor de tipo integer que representa el mes de la fecha especificada.
  
> [!NOTE]
> [!NOTA] La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Mes** (*Fecha*) 
  
La función **Month** contiene el siguiente argumento. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Date*  <br/> |Una expresión que se puede resolver en un valor Fecha/Hora.  <br/> |
   
## <a name="remarks"></a>Notas

 **Mes** devuelve el mismo valor que **DatePart** (mes, fecha). 
  
Si *fecha* contiene sólo una parte del tiempo, el valor devuelto es 1, el mes de base. 
  

