---
title: Función cosas (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición inicial y, a continuación, inserta la segunda cadena en la primera cadena en la posición inicial.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311028"
---
# <a name="stuff-function-access-custom-web-app"></a>Función cosas (aplicación web personalizada de Access)

Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición inicial y, a continuación, inserta la segunda cadena en la primera cadena en la posición inicial.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Cosas** (*IntoTextExpression*, *Start*, *length*, *ThisTextExpression*) 
  
La función **cosas** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Una expresión de texto que especifica el texto en el que se insertará el texto especificado por *ThisTextExpression* .  <br/> |
| *Start*  <br/> |Valor entero que especifica la ubicación en la que se iniciará la eliminación y la inserción. Si Start o length es negativo, se devuelve una cadena null. Si Start es superior a la primera *IntoTextExpression* , se devuelve una cadena null.  <br/> |
| *Length*  <br/> |Un entero que especifica el número de caracteres que se van a eliminar. Si length es superior a la primera *IntoTextExpression* , la eliminación se produce hasta el último carácter del último *IntoTextExpression* .  <br/> |
| *ThisTextExpression*  <br/> |Una expresión de texto Hat especifica el texto que se va a insertar en *IntoTextExpression* . Esta expresión reemplazará los caracteres de longitud de *IntoTextExpression* comenzando en *Start* .  <br/> |
   
## <a name="remarks"></a>Comentarios

Si los argumentos *Start* o *length* son negativos, o si la posición inicial es mayor que la longitud de la primera cadena, se devuelve una cadena null. Si la posición inicial es 0, se devuelve un valor null. Si la longitud que se va a eliminar es superior a la primera cadena, se elimina al primer carácter de la primera cadena. 
  

