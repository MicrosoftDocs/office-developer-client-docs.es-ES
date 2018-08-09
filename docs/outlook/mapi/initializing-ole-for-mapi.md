---
title: Inicializar OLE para MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817811"
---
# <a name="initializing-ole-for-mapi"></a>Inicializar OLE para MAPI

  
  
**Hace referencia a**: Outlook 
  
Si también utiliza OLE, llame a la función OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) para inicializar las bibliotecas OLE. **OleInitialize** inicializa datos globales para la sesión y prepara las bibliotecas OLE para aceptar llamadas. Para obtener información acerca de la llamada **OleInitialize**, vea el SDK de Windows.
  

