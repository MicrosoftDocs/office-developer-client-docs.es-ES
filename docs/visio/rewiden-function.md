---
title: REWIDEN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Convierte una fórmula que genera códigos de caracteres de 16 bits que son códigos ampliados de juego de caracteres de un byte o de varios bytes en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los conjuntos de caracteres especificado.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822993"
---
# <a name="rewiden-function"></a>REWIDEN (función)

Convierte una fórmula que genera códigos de caracteres de 16 bits que son códigos ampliados de juego de caracteres de un byte o de varios bytes en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los conjuntos de caracteres especificado. 
  
## <a name="syntax"></a>Sintaxis

REWIDEN (** *juegoCarOrig* **, ** *juegoCarDest* **, ** *texto* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _juegoCarOrig_ <br/> |Obligatorio  <br/> |**String** <br/> |El juego de caracteres del documento de origen.  <br/> |
| _juegoCarDest_ <br/> |Obligatorio  <br/> |**String** <br/> | El juego de caracteres del documento de destino.  <br/> |
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto que se debe convertir.  <br/> |
   
## <a name="remarks"></a>Observaciones

La función REWIDEN se usa en la conversión automática de documentos de Visio 2002 en documentos de Visio 2003 y no se recomienda ningún otro uso.
  

