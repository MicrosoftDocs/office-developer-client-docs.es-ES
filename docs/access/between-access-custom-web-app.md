---
title: ENTRE (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica un intervalo para probar.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815334"
---
# <a name="between-access-custom-web-app"></a>ENTRE (aplicación web personalizado de Access)

Especifica un intervalo para probar.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *test_expression*  [NOT] **BETWEEN** *begin_expression* **AND** *end_expression* 
  
El operador **entre** contiene los siguientes argumentos. 
  
|**Argumento**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Sí  <br/> |La expresión para la prueba en el intervalo definido mediante *begin_expression* y *end_expression* . Debe ser del mismo tipo de datos como *begin_expression* y *end_expression* .  <br/> |
| *NOT*  <br/> |No  <br/> |Especifica que se niega el resultado del predicado.  <br/> |
| *begin_expression*  <br/> |Sí  <br/> |Una expresión válida. Debe ser del mismo tipo de datos que *test_expression* y *end_expression* .  <br/> |
| *end_expression*  <br/> |Sí  <br/> |Una expresión válida. Debe ser del mismo tipo de datos que *test_expression* y *begin_expression* .  <br/> |
| *AND*  <br/> |Sí  <br/> |Indica que *test_expression* debe estar dentro del intervalo indicado por *begin_expression* y *end_expression* .  <br/> |
   
## <a name="result-type"></a>Tipo de resultado

 **Boolean**
  
## <a name="remarks"></a>Comentarios

 **BETWEEN** devuelve **TRUE** si el valor de *test_expression* es mayor o igual que el valor de *begin_expression* y menor o igual que el valor de *end_expression* . 
  
 **NOT BETWEEN** devuelve **TRUE** si el valor de *test_expression* es menor que el valor de *begin_expression* o mayor que el valor de *end_expression* . 
  
Para especificar un intervalo exclusivo, use el mayor que (\>) operadores y menor que (\<).
  

