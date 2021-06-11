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
description: Devuelve la fecha representada por año, mes y día con formato de acuerdo con el estilo de fecha corto en la configuración regional del Configuración. Los valores de año, mes y día reflejan el calendario gregoriano.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360336"
---
# <a name="date-function-visioshapesheet"></a>Función DATE (VisioShapeSheet)

Devuelve la fecha representada por *año, mes* y *día* con formato de acuerdo con el estilo de fecha corto en la configuración regional del Configuración. Los valores de  *año,* *mes*  y  *día*  reflejan el calendario gregoriano. 
  
## <a name="syntax"></a>Sintaxis

DATE(** *year* **, ** *month* **, ** *day* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El año.  <br/> |
| _month_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El mes.  <br/> |
| _day_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El día.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

DATE(1999,6,7)
  
Devuelve el valor que corresponde al 07/06/99.
  
## <a name="example-2"></a>Ejemplo 2

DATE(1999;6;7) + 4 ed.
  
Devuelve el valor que corresponde al 11/06/99.
  
## <a name="example-3"></a>Ejemplo 3

FORMAT(DATE(1999,10,14),"C")
  
Devuelve el valor que corresponde al 14/10/99.
  

