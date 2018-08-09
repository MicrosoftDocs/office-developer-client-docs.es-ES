---
title: Función DateWithTimeFromParts (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Devuelve una hora, fecha y hora en función de un año especificado, el mes, día.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815292"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Función DateWithTimeFromParts (aplicación web personalizado de Access)

Devuelve una hora, fecha y hora en función de un año especificado, el mes, día.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**DateWithTimeFromParts** (*Año*, *mes*, *día*, *hora*, *minuto*, *segundo*) 
  
La función **DateWithTimeFromParts** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *year*  <br/> |Expresión de tipo entero que especifica un año.  <br/> |
| *Month*  <br/> |Expresión de tipo entero que especifica un mes.  <br/> |
| *Día*  <br/> |Expresión de tipo entero que especifica un día.  <br/> |
| *Hora*  <br/> |Expresión de tipo Integer que especifica horas.  <br/> |
| *Minuto*  <br/> |Expresión de tipo Integer que especifica los minutos.  <br/> |
| *Segundo*  <br/> |Expresión de tipo Integer que especifica los segundos.  <br/> |
   
## <a name="remarks"></a>Comentarios

**DateWithTimeFromParts** devuelve un valor de fecha y hora totalmente inicializado. Si los argumentos no son válidos, se produce un error. Si es necesario argumentos son Null, se devuelve Null. 
  

