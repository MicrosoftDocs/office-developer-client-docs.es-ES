---
title: Función Try_Convert (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815526"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Función Try_Convert (aplicación web personalizado de Access)

Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Try_Convert** (*Tipo de datos*, *expresión*) 
  
La función **Try_Convert** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *DataType*  <br/> |El tipo de datos en el que se va a convertir *expresión* .  <br/> |
| *Expresión*  <br/> |El valor que se va a convertir.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **Try_Convert** toma el valor que se pasa a ella e intenta convertir en el *tipo de datos* de especificado. Si la conversión se realiza correctamente, **Try_Convert** devuelve el valor como el *tipo de datos* de especificado; Si se produce un error, se devuelve null. Sin embargo si solicita una conversión explícitamente no está permitido, a continuación, **Try_Convert** se produce un error con un error. 
  

