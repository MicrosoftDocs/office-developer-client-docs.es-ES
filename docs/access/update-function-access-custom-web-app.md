---
title: Función de actualización (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Devuelve si se intentó una operación INSERT o UPDATE en el campo especificado.
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815521"
---
# <a name="update-function-access-custom-web-app"></a>Función de actualización (aplicación web personalizado de Access)

Devuelve si se intentó una operación INSERT o UPDATE en el campo especificado.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Actualización** (*Columna*) 
  
La función de **actualización** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Column*  <br/> |El nombre del campo para comprobar si una operación INSERT o UPDATE.  <br/> |
   
## <a name="remarks"></a>Comentarios

La función de **actualización** devuelve el valor TRUE, independientemente de si un intento de INSERCIÓN o actualización es correcto. 
  

