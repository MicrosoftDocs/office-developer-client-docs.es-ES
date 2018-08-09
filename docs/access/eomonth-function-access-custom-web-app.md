---
title: Función EOMonth (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Devuelve el último día del mes antes o número de meses especificado.
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815313"
---
# <a name="eomonth-function-access-custom-web-app"></a>Función EOMonth (aplicación web personalizado de Access)

Devuelve el último día del mes antes o número de meses especificado.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **EOMonth** (*Fecha*, *NumberOfMonth*) 
  
El **EOMonth** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Date*  <br/> |La fecha en formato de fecha y hora, o en una representación de texto aceptados de una fecha de inicio.  <br/> |
| *NumberOfMonth*  <br/> |Un número que representa el número de meses antes o después de la *fecha* .  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la *fecha* no es una fecha válida, **EOMonth** devuelve un error. 
  
Si la *fecha* más *NumberOfMonth* da como resultado una fecha no válida, **EOMonth** devuelve un error. 
  

