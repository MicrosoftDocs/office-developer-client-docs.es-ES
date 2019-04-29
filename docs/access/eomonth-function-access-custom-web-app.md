---
title: Función de fin de mes (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Devuelve el último día del mes antes o especifica el número de meses.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437458"
---
# <a name="eomonth-function-access-custom-web-app"></a>Función de fin de mes (aplicación web personalizada de Access)

Devuelve el último día del mes antes o especifica el número de meses.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Fin de mes** (*Fecha*, *NumberOfMonth*) 
  
El **mes** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Date*  <br/> |La fecha de inicio en el formato de fecha y hora, o en una representación de texto aceptada de una fecha.  <br/> |
| *NumberOfMonth*  <br/> |Un número que representa el número de meses antes o después de la *fecha* .  <br/> |
   
## <a name="remarks"></a>Comentarios

Si *fecha* no es una fecha válida, **fin de mes** devuelve un error. 
  
Si *fecha* más *NumberOfMonth* da como resultado una fecha no válida, **fin de mes** devuelve un error. 
  

