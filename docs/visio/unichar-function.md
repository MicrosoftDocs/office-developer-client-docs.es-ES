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
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823481"
---
# <a name="unichar-function"></a>Función UNICHAR

Devuelve el carácter Unicode de un número. 
  
## <a name="syntax"></a>Sintaxis

UNICHAR (** *número* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Debe ser un entero comprendido entre 1 y 65.535 (ambos inclusive), o la función devuelve un error.  <br/> |
   
## <a name="remarks"></a>Observaciones

La cadena resultante tiene un carácter Unicode (dos caracteres) de longitud. 
  
## <a name="example"></a>Ejemplo

UNICHAR(65) 
  
Devuelve un (letra latina mayúscula A) 
  

