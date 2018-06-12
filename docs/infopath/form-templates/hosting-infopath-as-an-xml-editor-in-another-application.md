---
title: Hospedar InfoPath como un editor XML en otra aplicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: El entorno de edición de formulario de Microsoft InfoPath se puede hospedar en una aplicación de Windows personalizada, que permite a los programadores integrar el entorno en aplicaciones de línea de negocio de edición de formularios de InfoPath.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815857"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hospedar InfoPath como un editor XML en otra aplicación

El entorno de edición de formularios de Microsoft InfoPath puede hospedarse en una aplicación para Windows personalizada. Esta característica permite a los programadores integrar el entorno de edición de formularios de InfoPath en las aplicaciones de la línea de negocio. Los programadores que crean aplicaciones tradicionales basadas en COM pueden usar el objeto **InfoPathEditorObject**, disponible si se hace referencia a IPEDITOR.DLL, y los programadores que escriben aplicaciones basadas en Microsoft .NET pueden usar el ensamblado **Microsoft.Office.InfoPath.FormControl**, que proporciona tipos administrados basados en la interfaz COM. El archivo IPEDITOR.DLL y el ensamblado **Microsoft.Office.InfoPath.FormControl** se instalan junto con InfoPath en la carpeta C:\Program Files\Microsoft Office\Office15 o C:\Program Files (x86)\Microsoft Office\Office15 . 
  
El artículo de MSDN, que hospeda el entorno de edición de formulario de InfoPath 2007 en una aplicación de formularios de Windows personalizada, se centra en el objeto **FormControl** y cómo incorporarla a personalizado. Aplicaciones basadas en red. Asociado a este artículo hay una aplicación personalizada que se puede descargar y que ofrece funciones de .NET para replicar el entorno de edición de formularios mediante el uso de **IOleCommandTargets** de COM.
  

