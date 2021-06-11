---
title: Función Count (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Devuelve el número de registros de una consulta o tabla.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419145"
---
# <a name="count-function-access-custom-web-app"></a>Función Count (aplicación web personalizada de Access)

Devuelve el número de registros de una consulta o tabla.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**Count** (*Expresión*) 
  
La **función Count** contiene el siguiente argumento. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Expresión*  <br/> |Expresión de cadena que identifica el campo que contiene los datos que desea contar o una expresión que realiza un cálculo con los datos del campo. Los operandos de *Expresión* pueden incluir el nombre de un campo o función de tabla (que puede ser intrínseco o definido por el usuario, pero no otras funciones SQL agregado). Se pueden contar todo tipo de datos, incluido texto.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede usar Count para contar el número de registros de una consulta base. Por ejemplo, puede usar Count para contar el número de pedidos enviados a una región o país determinado.
  
**Count** ( \* ) devuelve el número de elementos de un grupo. Esto incluye valores NULL y duplicados. 
  

