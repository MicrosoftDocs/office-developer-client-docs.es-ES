---
title: DOOLEVERB (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Ejecuta un verbo para el objeto OLE.
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822015"
---
# <a name="dooleverb-function"></a>DOOLEVERB (función)

Ejecuta un verbo para el objeto OLE.
  
## <a name="syntax"></a>Sintaxis

DOOLEVERB ("** *verbo* **") 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _"verbo"_ <br/> |Obligatorio  <br/> |**String** <br/> |Verbo para ejecutar.  <br/> |
   
## <a name="remarks"></a>Observaciones

En versiones anteriores de Visio, esta función se denominaba _DOOLEVERB. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones. 
  
## <a name="example"></a>Ejemplo

DOOLEVERB("edit")
  
Ejecuta el programa del objeto OLE y muestra el objeto vinculado o incrustado de forma que pueda modificarse.
  

