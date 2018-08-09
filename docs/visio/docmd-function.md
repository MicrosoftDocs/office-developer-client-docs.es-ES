---
title: DOCMD (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Ejecuta el comando identificado.
ms.openlocfilehash: e425dd9605c18d4647787c5df7aeaa4fd5f9e4cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821999"
---
# <a name="docmd-function"></a>Función DOCMD

Ejecuta el comando identificado.
  
## <a name="syntax"></a>Sintaxis

 **DOCMD** ( _IDcomando_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _IDcomando_ <br/> |Obligatorio  <br/> |**Número** <br/> | Comando que se debe ejecutar.  <br/> |
   
## <a name="remarks"></a>Observaciones

Para obtener una lista de comandos que son compatibles con la función DOCMD, vea el tema "Comandos DoCmd/DOCMD" en la referencia de automatización de Microsoft Visio 2013. 
  
## <a name="example"></a>Ejemplo

 `DOCMD (1312)`
  
Hace que el cuadro de diálogo **Datos de formas** aparezca en la interfaz de usuario. 
  

