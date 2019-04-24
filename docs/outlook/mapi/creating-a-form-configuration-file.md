---
title: Creación de un archivo de configuración de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333022"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="78627-103">Creación de un archivo de configuración de formulario</span><span class="sxs-lookup"><span data-stu-id="78627-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="78627-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78627-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78627-105">Un archivo de configuración de formulario proporciona información sobre un formulario tanto al administrador de formularios que se utiliza como a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="78627-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="78627-106">Un archivo de configuración de formulario contiene una completa especificación para un formulario, incluidas las propiedades publicadas por el formulario para que las usen los clientes de mensajería, los verbos implementados por el formulario y las plataformas admitidas por el formulario.</span><span class="sxs-lookup"><span data-stu-id="78627-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="78627-107">Un archivo de configuración de formulario es un archivo con una extensión. cfg y tiene un formato similar a un archivo de inicialización de Windows.</span><span class="sxs-lookup"><span data-stu-id="78627-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="78627-108">Se trata de un archivo de texto sin formato con una serie de secciones.</span><span class="sxs-lookup"><span data-stu-id="78627-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="78627-109">Cada sección comienza con un nombre de sección, entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="78627-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="78627-110">Cada sección contiene una o varias líneas que definen los valores y la configuración relevantes para dicha sección.</span><span class="sxs-lookup"><span data-stu-id="78627-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="78627-111">Los valores tienen uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="78627-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="78627-112">String</span><span class="sxs-lookup"><span data-stu-id="78627-112">String</span></span>
    
- <span data-ttu-id="78627-113">Cadena mostrada</span><span class="sxs-lookup"><span data-stu-id="78627-113">Displayed string</span></span>
    
- <span data-ttu-id="78627-114">Cadena de la plataforma</span><span class="sxs-lookup"><span data-stu-id="78627-114">Platform string</span></span>
    
- <span data-ttu-id="78627-115">Nombre de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="78627-115">Path name</span></span>
    
- <span data-ttu-id="78627-116">Entero</span><span class="sxs-lookup"><span data-stu-id="78627-116">Integer</span></span>
    
- <span data-ttu-id="78627-117">GUID</span><span class="sxs-lookup"><span data-stu-id="78627-117">GUID</span></span>
    
<span data-ttu-id="78627-118">Para obtener más información acerca de las secciones de un archivo. cfg, vea el [formato de archivo de los archivos de configuración de formulario](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="78627-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78627-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="78627-119">See also</span></span>



[<span data-ttu-id="78627-120">Desarrollar servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="78627-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

