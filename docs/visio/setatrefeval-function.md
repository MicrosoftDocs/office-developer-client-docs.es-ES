---
title: SETATREFEVAL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Se usa en el parámetro expresión_conjunto de la función SETATREF para indicar que expresión_conjunto debe evaluarse antes de asignarse al parámetro de referencia en SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326162"
---
# <a name="setatrefeval-function"></a>Función SETATREFEVAL

Se usa en el parámetro _expresión_conjunto_ de la función SETATREF para indicar que _expresión_conjunto_ debe evaluarse antes de asignarse al parámetro de _referencia_ en SETATREF. 
  
## <a name="syntax"></a>Sintaxis

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obligatorio  <br/> |**Diferencias** <br/> | Expresión que se evalúa cuando la función SETATREF redirige _expresión_conjunto_ a otra celda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se asigna el parámetro *expresión_conjunto* de la función SETATREF a una celda a la que se hace referencia, Microsoft Visio escribe *expresión_conjunto* en la celda como una expresión de forma predeterminada. Sin embargo, si alguna parte del parámetro *expresión_conjunto* está ajustada por la función Setatrefeval, Visio evalúa la expresión y reemplaza la función setatrefeval por el resultado antes de resolver la expresión SETATREF. 
  
## <a name="example"></a>Ejemplo

Para conocer un ejemplo, vea el tema que trata la función [SETATREF](setatref-function.md). 
  

