---
title: Función Count (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Devuelve el número de registros de una tabla o consulta.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815343"
---
# <a name="count-function-access-custom-web-app"></a>Función Count (aplicación web personalizado de Access)

Devuelve el número de registros de una tabla o consulta.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**Recuento** (*Expresión*) 
  
La función **Count** contiene el siguiente argumento. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Expresión*  <br/> |Una expresión de cadena que identifica el campo que contiene los datos que desea count o una expresión que realiza un cálculo utilizando los datos en el campo. Operandos de *expresión* pueden incluir el nombre de un campo de tabla o una función (que puede ser intrínseca o definida por el usuario pero no otra SQL funciones de agregado). Se pueden contar todo tipo de datos, incluido texto.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede usar Count para contar el número de registros de una consulta base. Por ejemplo, puede usar Count para contar el número de pedidos enviados a una región o país determinado.
  
**Recuento** (\*) devuelve el número de elementos de un grupo. Esto incluye valores NULL y duplicados. 
  

