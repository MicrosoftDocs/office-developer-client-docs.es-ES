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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425221"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="7857f-103">Creación de un archivo de configuración de formulario</span><span class="sxs-lookup"><span data-stu-id="7857f-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="7857f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7857f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7857f-105">Un archivo de configuración de formulario proporciona información acerca de un formulario tanto al administrador de formularios que se usa como a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="7857f-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="7857f-106">Un archivo de configuración de formulario contiene una amplia especificación para un formulario, incluidas las propiedades publicadas por el formulario para su uso por clientes de mensajería, los verbos implementados por el formulario y las plataformas admitidas por el formulario.</span><span class="sxs-lookup"><span data-stu-id="7857f-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="7857f-107">Un archivo de configuración de formulario es un archivo con extensión .cfg y tiene un formato similar a un archivo de inicialización de Windows.</span><span class="sxs-lookup"><span data-stu-id="7857f-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="7857f-108">Es un archivo de texto sin formato con varias secciones.</span><span class="sxs-lookup"><span data-stu-id="7857f-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="7857f-109">Cada sección comienza con un nombre de sección, entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="7857f-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="7857f-110">Cada sección contiene una o más líneas que definen valores y configuraciones relevantes para esa sección.</span><span class="sxs-lookup"><span data-stu-id="7857f-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="7857f-111">Los valores tienen uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="7857f-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="7857f-112">String</span><span class="sxs-lookup"><span data-stu-id="7857f-112">String</span></span>
    
- <span data-ttu-id="7857f-113">Cadena mostrada</span><span class="sxs-lookup"><span data-stu-id="7857f-113">Displayed string</span></span>
    
- <span data-ttu-id="7857f-114">Cadena de plataforma</span><span class="sxs-lookup"><span data-stu-id="7857f-114">Platform string</span></span>
    
- <span data-ttu-id="7857f-115">Nombre de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="7857f-115">Path name</span></span>
    
- <span data-ttu-id="7857f-116">Entero</span><span class="sxs-lookup"><span data-stu-id="7857f-116">Integer</span></span>
    
- <span data-ttu-id="7857f-117">GUID</span><span class="sxs-lookup"><span data-stu-id="7857f-117">GUID</span></span>
    
<span data-ttu-id="7857f-118">Para obtener más información acerca de las secciones de un archivo .cfg, vea Formato de archivo [de archivos de configuración de formulario.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="7857f-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7857f-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7857f-119">See also</span></span>



[<span data-ttu-id="7857f-120">Desarrollo de servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="7857f-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

