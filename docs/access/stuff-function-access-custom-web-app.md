---
title: Función de material (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815494"
---
# <a name="stuff-function-access-custom-web-app"></a>Función de material (aplicación web personalizado de Access)

Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Syntax

 **Cosas** (*IntoTextExpression*, *Inicio*, *longitud*, *ThisTextExpression*) 
  
La función **cosas** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Una expresión de texto que especifica el texto en el que se va a insertar el texto especificado por el *ThisTextExpression* .  <br/> |
| *Start*  <br/> |Un valor entero que especifica la ubicación para iniciar la inserción y eliminación. Si start o length es negativo, se devuelve una cadena null. Si start es mayor que el primer *IntoTextExpression* , se devuelve una cadena null.  <br/> |
| *Length*  <br/> |Un entero que especifica el número de caracteres que se va a eliminar. Si length es mayor que el primer *IntoTextExpression* , se produce la eliminación hasta el último carácter de la última *IntoTextExpression* .  <br/> |
| *ThisTextExpression*  <br/> |Un acento circunflejo expresión de texto especifica el texto para insertar en *IntoTextExpression* . Esta expresión reemplazará los caracteres de longitud de *Inicio* a partir de *IntoTextExpression* .  <br/> |
   
## <a name="remarks"></a>Notas

Si los argumentos *Iniciar* o *Length* son negativos, o si la posición inicial es mayor que la longitud de la primera cadena, se devuelve una cadena nula. Si la posición inicial es 0, se devuelve un valor nulo. Si la longitud para eliminar es mayor que la primera cadena, se elimina hasta el primer carácter de la primera cadena. 
  

