---
title: Creación de un archivo de configuración de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816614"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="13ac5-103">Creación de un archivo de configuración de formulario</span><span class="sxs-lookup"><span data-stu-id="13ac5-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="13ac5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13ac5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13ac5-105">Un archivo de configuración de formulario proporciona información acerca de un formulario para el Administrador de formulario que se usa y a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="13ac5-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="13ac5-106">Un archivo de configuración de formulario contiene una especificación de una amplia para un formulario, incluidas las propiedades publicadas por el formulario para su uso por parte de mensajería los clientes, los verbos de implementada por el formulario y las plataformas compatibles con el formulario.</span><span class="sxs-lookup"><span data-stu-id="13ac5-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="13ac5-107">Un archivo de configuración de formulario es un archivo con una extensión .cfg y tiene un formato similar a un archivo de inicialización de Windows.</span><span class="sxs-lookup"><span data-stu-id="13ac5-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="13ac5-108">Es un archivo de texto sin formato con un número de secciones.</span><span class="sxs-lookup"><span data-stu-id="13ac5-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="13ac5-109">Cada sección comienza con un nombre de sección, entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="13ac5-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="13ac5-110">Cada sección contiene una o varias líneas que definen los valores y opciones relevantes para esa sección.</span><span class="sxs-lookup"><span data-stu-id="13ac5-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="13ac5-111">Los valores de tengan uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="13ac5-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="13ac5-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="13ac5-112">String</span></span>
    
- <span data-ttu-id="13ac5-113">Cadena que se muestra</span><span class="sxs-lookup"><span data-stu-id="13ac5-113">Displayed string</span></span>
    
- <span data-ttu-id="13ac5-114">Cadena de plataforma</span><span class="sxs-lookup"><span data-stu-id="13ac5-114">Platform string</span></span>
    
- <span data-ttu-id="13ac5-115">Nombre de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="13ac5-115">Path name</span></span>
    
- <span data-ttu-id="13ac5-116">Entero</span><span class="sxs-lookup"><span data-stu-id="13ac5-116">Integer</span></span>
    
- <span data-ttu-id="13ac5-117">GUID</span><span class="sxs-lookup"><span data-stu-id="13ac5-117">GUID</span></span>
    
<span data-ttu-id="13ac5-118">Para obtener más información acerca de las secciones de un archivo .cfg, vea el [Archivo de formato de formulario de los archivos de configuración](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="13ac5-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="13ac5-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="13ac5-119">See also</span></span>



[<span data-ttu-id="13ac5-120">Desarrollo de los servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="13ac5-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

