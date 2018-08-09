---
title: Formato de archivo de los archivos de configuración de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: def91b4e28e60f6d2e8534f0ed7261777ec0c8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816798"
---
# <a name="file-format-of-form-configuration-files"></a>Formato de archivo de los archivos de configuración de formulario

**Hace referencia a**: Outlook 
  
Un archivo de configuración de formulario es un archivo con formato creado por los programadores de formularios para definir un formulario.
  
Debido a que los archivos de configuración de formulario se utilizan los administradores de formulario para cargar formularios, debe definirse cada formulario mediante un archivo de configuración del formulario. Los archivos de configuración de formulario deben tener la extensión de nombre de archivo .cfg. El archivo sigue la sintaxis general de un archivo de inicialización (. ini archivo) de Windows. 

Se divide en secciones con nombre, y cada sección contiene una serie de entradas y valores. Los valores de tengan uno de los siguientes tipos: cadena, una cadena que se muestra, cadena de plataforma, ruta de acceso, número entero o identificador único global, **GUID**. Los archivos de configuración de formulario se pueden crear con cualquier editor de texto o un procesador de textos que es capaz de guardar archivos de texto.
  

