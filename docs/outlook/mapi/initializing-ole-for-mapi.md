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
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388424"
---
# <a name="initializing-ole-for-mapi"></a>Inicializar OLE para MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Si también utiliza OLE, llame a la función OLE [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) para inicializar las bibliotecas OLE. **OleInitialize** inicializa datos globales para la sesión y prepara las bibliotecas OLE para aceptar llamadas. Para obtener información acerca de la llamada **OleInitialize**, vea el SDK de Windows.
  

