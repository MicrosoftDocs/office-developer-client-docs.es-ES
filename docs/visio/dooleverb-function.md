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
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435665"
---
# <a name="dooleverb-function"></a>Función DOOLEVERB

Ejecuta un verbo para el objeto OLE.
  
## <a name="syntax"></a>Sintaxis

DOOLEVERB ("* * *verbo* * *") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _verbo_ <br/> |Obligatorio  <br/> |**String** <br/> |Verbo para ejecutar.  <br/> |
   
## <a name="remarks"></a>Comentarios

En versiones anteriores de Visio, esta función se denominaba _DOOLEVERB. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones. 
  
## <a name="example"></a>Ejemplo

DOOLEVERB ("edición")
  
Ejecuta el programa del objeto OLE y muestra el objeto vinculado o incrustado de forma que pueda modificarse.
  

