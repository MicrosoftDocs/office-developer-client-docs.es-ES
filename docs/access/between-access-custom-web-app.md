---
title: BETWEEN (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica un intervalo que se va a probar.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429302"
---
# <a name="between-access-custom-web-app"></a>BETWEEN (aplicación web personalizada de Access)

Especifica un intervalo que se va a probar.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *test_expression* [ NOT ] **ENTRE begin_expression**  **Y end_expression**  
  
El **operador Between** contiene los argumentos siguientes. 
  
|**Argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Sí  <br/> |Expresión que se va a probar en el intervalo definido por  *begin_expression*  y  *end_expression*  . Debe ser el mismo tipo de datos que  *begin_expression*  y  *end_expression*  .  <br/> |
| *NOT*  <br/> |No  <br/> |Especifica que se niega el resultado del predicado.  <br/> |
| *begin_expression*  <br/> |Sí  <br/> |Expresión válida. Debe ser el mismo tipo de datos que  *test_expression*  y  *end_expression*  .  <br/> |
| *end_expression*  <br/> |Sí  <br/> |Expresión válida. Debe ser el mismo tipo de datos que  *test_expression*  y  *begin_expression*  .  <br/> |
| *Y*  <br/> |Sí  <br/> |Indica que  *test_expression*  debe estar dentro del intervalo indicado por  *begin_expression*  y  *end_expression*  .  <br/> |
   
## <a name="result-type"></a>Tipo de resultado

 **Boolean**
  
## <a name="remarks"></a>Comentarios

 **BETWEEN** devuelve **TRUE** si el valor de  *test_expression*  es mayor o igual que el valor de  *begin_expression*  y menor o igual que el valor de  *end_expression*  . 
  
 **NOT BETWEEN** devuelve **TRUE** si el valor de  *test_expression*  es menor que el valor de  *begin_expression*  o mayor que el valor de  *end_expression*  . 
  
Para especificar un intervalo exclusivo, use el valor mayor que ( \> ) y menor que los operadores ( \< ).
  

