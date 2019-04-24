---
title: UNICHAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Devuelve el carácter Unicode de un número.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327352"
---
# <a name="unichar-function"></a>Función UNICHAR

Devuelve el carácter Unicode de un número. 
  
## <a name="syntax"></a>Sintaxis

UniCHAR (* * *número* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Debe ser un entero comprendido entre 1 y 65.535 (ambos inclusive), o la función devuelve un error.  <br/> |
   
## <a name="remarks"></a>Comentarios

La cadena resultante tiene un carácter Unicode (dos caracteres) de longitud. 
  
## <a name="example"></a>Ejemplo

UNICHAR (65) 
  
Devuelve A (letra A mayúscula latina) 
  

