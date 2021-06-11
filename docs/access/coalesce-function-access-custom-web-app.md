---
title: Función Coalesce (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Devuelve la primera expresión que no es NULL de una lista de argumentos.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411396"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="53e14-103">Función Coalesce (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="53e14-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="53e14-104">Devuelve la primera expresión que no es NULL de una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="53e14-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="53e14-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="53e14-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="53e14-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53e14-107">Syntax</span></span>

<span data-ttu-id="53e14-108">**Coalesce** (*Value*, [*Value*], ...,[*Value*])</span><span class="sxs-lookup"><span data-stu-id="53e14-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="53e14-109">La **función Coalesce** contiene los argumentos siguientes</span><span class="sxs-lookup"><span data-stu-id="53e14-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="53e14-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="53e14-110">**Argument name**</span></span>|<span data-ttu-id="53e14-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53e14-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="53e14-112">*Valor*</span><span class="sxs-lookup"><span data-stu-id="53e14-112">*Value*</span></span>  <br/> |<span data-ttu-id="53e14-113">Expresión.</span><span class="sxs-lookup"><span data-stu-id="53e14-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53e14-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53e14-114">Remarks</span></span>

<span data-ttu-id="53e14-115">Si todos los argumentos son NULL, **Coalesce** devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="53e14-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="53e14-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53e14-116">Example</span></span>

<span data-ttu-id="53e14-117">La siguiente expresión se usa como regla de validación para una tabla.</span><span class="sxs-lookup"><span data-stu-id="53e14-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="53e14-118">La expresión garantiza que las entradas se realizan en los campos Nombre, Apellido, Correo electrónico, Teléfono móvil, Trabajo Teléfono, Inicio Teléfono y Empresa antes de que se confirma un registro.</span><span class="sxs-lookup"><span data-stu-id="53e14-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="53e14-119">Si alguno de los campos enumerados se deja en blanco, la función **Coalesce** devuelve Null, lo que infringe la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="53e14-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


