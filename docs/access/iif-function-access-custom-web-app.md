---
title: Función IIf (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Comprueba si se cumple una condición y devuelve un valor si es TRUE de otro si es FALSE.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439082"
---
# <a name="iif-function-access-custom-web-app"></a>Función IIf (aplicación web personalizada de Access)

Comprueba si se cumple una condición y devuelve un valor si es TRUE de otro si es FALSE.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**IIf** (*Condition*, *TrueValue*, *FalseValue*) 
  
La **función IIf** contiene los argumentos siguientes. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Condition*  <br/> |Expresión que desea evaluar.  <br/> |
| *TrueValue*  <br/> |Valor o expresión devueltos  *si Condition*  es True.  <br/> |
| *FalseValue*  <br/> |Valor o expresión devueltos si  *Condition*  es False.  <br/> |
   
## <a name="example"></a>Ejemplo

La siguiente expresión puede usarse para mostrar el nombre completo de una persona en la tabla que contiene los campos Nombre, Segundo nombre y Apellidos. Si el campo Segundo nombre está en blanco, los campos Nombre y Apellidos se combinan para mostrar el nombre completo,
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


