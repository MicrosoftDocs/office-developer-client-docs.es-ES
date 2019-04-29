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
description: Convierte una fórmula que produce códigos de caracteres de 16 bits que son códigos de conjunto de caracteres de un byte o multibyte ampliados en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los juegos de caracteres especificados.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405215"
---
# <a name="rewiden-function"></a>Función REWIDEN

Convierte una fórmula que produce códigos de caracteres de 16 bits que son códigos de conjunto de caracteres de un byte o multibyte ampliados en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los juegos de caracteres especificados. 
  
## <a name="syntax"></a>Sintaxis

ReWIDEn (* * *srcCharSet* * *, * * *dstCharSet* * *, * * *Text* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Obligatorio  <br/> |**String** <br/> |El juego de caracteres del documento de origen.  <br/> |
| _dstCharSet_ <br/> |Obligatorio  <br/> |**String** <br/> | El juego de caracteres del documento de destino.  <br/> |
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto que se debe convertir.  <br/> |
   
## <a name="remarks"></a>Comentarios

La función REWIDEN se usa en la conversión automática de documentos de Visio 2002 en documentos de Visio 2003 y no se recomienda ningún otro uso.
  

