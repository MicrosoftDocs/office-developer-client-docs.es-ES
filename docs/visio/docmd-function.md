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
description: Realiza el comando identificado.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413076"
---
# <a name="docmd-function"></a>Función DOCMD

Realiza el comando identificado.
  
## <a name="syntax"></a>Sintaxis

 **DOCMD**( _commandID_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _commandID_ <br/> |Obligatorio  <br/> |**Number** <br/> | Comando que se debe ejecutar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una lista de comandos compatibles con la función DOCMD, vea el tema "Comandos DoCmd/DOCMD" en la Referencia de automatización de Microsoft Visio 2013. 
  
## <a name="example"></a>Ejemplo

 `DOCMD (1312)`
  
Hace que el cuadro de diálogo **Datos de formas** aparezca en la interfaz de usuario. 
  

