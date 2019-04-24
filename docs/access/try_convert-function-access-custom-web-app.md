---
title: Función Try_Convert (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convierte un valor en un tipo de datos especificado o devuelve NULL si la conversión no es válida.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304231"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Función Try_Convert (aplicación web personalizada de Access)

Convierte un valor en un tipo de datos especificado o devuelve NULL si la conversión no es válida.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Try_Convert** (*DataType*, *expresión*) 
  
La función **Try_Convert** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *DataType*  <br/> |Tipo de datos en el que se va a convertir la *expresión* .  <br/> |
| *Expression*  <br/> |Valor que se va a convertir.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **Try_Convert** toma el valor que se ha pasado e intenta convertirlo en el *tipo de texto* especificado. Si la conversión se realiza correctamente, **Try_Convert** devuelve el valor como el *tipo de tipodedatos* especificado; Si se produce un error, se devuelve NULL. Sin embargo, si solicita una conversión que no está permitida explícitamente, **Try_Convert** produce un error. 
  

