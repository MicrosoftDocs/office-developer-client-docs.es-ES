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
ms.openlocfilehash: d07d88d7b8b892a82832f91989e322ea3b32e040
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415554"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="23094-103">Formato de archivo de los archivos de configuración de formulario</span><span class="sxs-lookup"><span data-stu-id="23094-103">File format of form configuration files</span></span>

<span data-ttu-id="23094-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23094-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23094-105">Un archivo de configuración de formulario es un archivo con formato creado por programadores de formularios para definir un formulario.</span><span class="sxs-lookup"><span data-stu-id="23094-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="23094-106">Dado que los administradores de formularios usan los archivos de configuración de formulario para cargar formularios, cada formulario debe definirse mediante un archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="23094-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="23094-107">Los archivos de configuración del formulario deben tener la extensión de nombre de archivo .cfg.</span><span class="sxs-lookup"><span data-stu-id="23094-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="23094-108">El archivo sigue la sintaxis general de un archivo de inicialización de Windows (archivo .ini).</span><span class="sxs-lookup"><span data-stu-id="23094-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="23094-109">Se divide en secciones con nombre y cada sección contiene una serie de entradas y valores.</span><span class="sxs-lookup"><span data-stu-id="23094-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="23094-110">Los valores tienen uno de los siguientes tipos: cadena, cadena mostrada, cadena de plataforma, ruta de acceso, entero o identificador único global, **GUID**.</span><span class="sxs-lookup"><span data-stu-id="23094-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="23094-111">Los archivos de configuración de formularios se pueden crear con cualquier editor de texto o procesador de texto que sea capaz de guardar archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="23094-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

