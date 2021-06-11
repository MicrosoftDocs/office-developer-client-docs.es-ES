---
title: Try_Convert (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410899"
---
# <a name="try_convert-function-access-custom-web-app"></a>Try_Convert (aplicación web personalizada de Access)

Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Try_Convert** (*DataType*, *Expression*) 
  
La **Try_Convert** contiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *DataType*  <br/> |Tipo de datos en el que se va a convertir  *Expression*  .  <br/> |
| *Expression*  <br/> |Valor que se va a convertir.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **Try_Convert** toma el valor que se le ha pasado e intenta convertirlo en el *DataType especificado.* Si la conversión se realiza **correctamente, Try_Convert** devuelve el valor como  *datatype especificado*  ; si se produce un error, se devuelve null. Sin embargo, si solicita una conversión que no está permitida explícitamente, **Try_Convert** error. 
  

