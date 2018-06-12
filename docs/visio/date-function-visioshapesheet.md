---
title: Función DATE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Devuelve la fecha representada por año, mes y día con el formato corresponde al estilo corto de fecha en la configuración Regional del sistema. Los valores de año, mes y día reflejan el calendario gregoriano.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821943"
---
# <a name="date-function-visioshapesheet"></a>Función DATE (VisioShapeSheet)

Devuelve la fecha representada por *año, mes* y *día* con el formato corresponde al estilo corto de fecha en la configuración Regional del sistema. Los valores de *año*, *mes* y *día* reflejan el calendario gregoriano. 
  
## <a name="syntax"></a>Sintaxis

FECHA (** *año* **, ** *mes* **, ** *día* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El año.  <br/> |
| _month_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El mes.  <br/> |
| _day_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El día.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

DATE(1999;6;7)
  
Devuelve el valor que corresponde al 07/06/99.
  
## <a name="example-2"></a>Ejemplo 2

DATE(1999;6;7) + 4 ed.
  
Devuelve el valor que corresponde al 11/06/99.
  
## <a name="example-3"></a>Ejemplo 3

FORMAT(DATE(1999,10,14),"C")
  
Devuelve el valor que corresponde al 14/10/99.
  

