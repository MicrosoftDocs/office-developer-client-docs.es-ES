---
title: Datos adjuntos OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: fb716ce014ec3c4b21ce2b021c1a9f6f291d511c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417150"
---
# <a name="ole-attachments"></a>Datos adjuntos OLE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Datos adjuntos que son objetos OLE se codifican como objetos stream de OLE 1 para compatibilidad con versiones anteriores. Si el objeto original es realmente un objeto de **IStorage** de OLE 2, se debe convertir el objeto en una secuencia de OLE 1. Esta conversi�n se realiza mediante la funci�n **OleConvertIStorageToOLESTREAM**, que forma parte de las bibliotecas de Win32 OLE. 
  

