---
title: Función DateWithTimeFromParts (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Devuelve una fecha y hora basadas en un año, mes, día y hora especificados.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422092"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Función DateWithTimeFromParts (aplicación web personalizada de Access)

Devuelve una fecha y hora basadas en un año, mes, día y hora especificados.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*) 
  
La **función DateWithTimeFromParts** contiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Year*  <br/> |Expresión de entero que especifica un año.  <br/> |
| *Month*  <br/> |Expresión de entero que especifica un mes.  <br/> |
| *Day*  <br/> |Expresión de número entero que especifica un día.  <br/> |
| *Hour*  <br/> |Expresión de entero que especifica horas.  <br/> |
| *Minute*  <br/> |Expresión de entero que especifica minutos.  <br/> |
| *Second*  <br/> |Expresión de entero que especifica segundos.  <br/> |
   
## <a name="remarks"></a>Comentarios

**DateWithTimeFromParts** devuelve un valor Date/Time completamente inicializado. Si los argumentos no son válidos, se genera un error. Si los argumentos necesarios son Null, se devuelve Null. 
  

