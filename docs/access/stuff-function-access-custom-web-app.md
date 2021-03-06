---
title: Función Stuff (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427678"
---
# <a name="stuff-function-access-custom-web-app"></a>Función Stuff (aplicación web personalizada de Access)

Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*) 
  
La **función Stuff** contiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Expresión de texto que especifica el texto en el que se insertará el texto especificado por *ThisTextExpression.*  <br/> |
| *Start*  <br/> |Valor entero que especifica la ubicación para iniciar la eliminación y la inserción. Si start o length es negativo, se devuelve una cadena nula. Si start es más largo que el primer  *Objeto IntoTextExpression*  , se devuelve una cadena nula.  <br/> |
| *Length*  <br/> |Entero que especifica el número de caracteres que se eliminarán. Si la longitud es mayor que la primera  *IntoTextExpression*  , la eliminación se produce hasta el último carácter del último  *IntoTextExpression*  .  <br/> |
| *ThisTextExpression*  <br/> |Un sombrero de expresión de texto especifica el texto que se insertará en  *IntoTextExpression*  . Esta expresión reemplazará los caracteres de longitud de  *IntoTextExpression a*  partir de  *Start*  .  <br/> |
   
## <a name="remarks"></a>Comentarios

Si los  *argumentos Start*  o  *Length*  son negativos, o si la posición inicial es mayor que la longitud de la primera cadena, se devuelve una cadena nula. Si la posición de inicio es 0, se devuelve un valor nulo. Si la longitud que se va a eliminar es mayor que la primera cadena, se elimina al primer carácter de la primera cadena. 
  

