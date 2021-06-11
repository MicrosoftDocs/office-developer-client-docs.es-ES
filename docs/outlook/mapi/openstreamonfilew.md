---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406027"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="dd77b-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="dd77b-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="dd77b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd77b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd77b-105">Asigna e inicializa un objeto OLE **IStream** para tener acceso al contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="dd77b-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="dd77b-106">Esta función toma cadenas UNICODE como argumentos, a diferencia de la versión ANSI de esta función [OpenStreamOnFile](openstreamonfile.md)y, por lo tanto, permite caracteres arbitrarios en el nombre del archivo, incluida la ruta de acceso y la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="dd77b-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd77b-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="dd77b-107">Exported by:</span></span>  <br/> |<span data-ttu-id="dd77b-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="dd77b-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="dd77b-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dd77b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd77b-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="dd77b-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="dd77b-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dd77b-111">Called by:</span></span>  <br/> |<span data-ttu-id="dd77b-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="dd77b-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="dd77b-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="dd77b-113">Parameters</span></span>

 <span data-ttu-id="dd77b-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="dd77b-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="dd77b-115">[in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="dd77b-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="dd77b-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="dd77b-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="dd77b-117">[in] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="dd77b-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="dd77b-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd77b-118">_ulFlags_</span></span>
  
> <span data-ttu-id="dd77b-119">[in] Máscara de bits de marcas usadas para controlar la creación o apertura del archivo al que se tiene acceso a través del objeto OLE **IStream.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="dd77b-120">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="dd77b-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="dd77b-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="dd77b-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="dd77b-122">Se creará un archivo temporal para el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="dd77b-123">Si se establece esta marca, también STGM_CREATE y STGM_READWRITE deben establecerse.</span><span class="sxs-lookup"><span data-stu-id="dd77b-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="dd77b-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="dd77b-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="dd77b-125">El archivo se va a crear incluso si ya existe uno.</span><span class="sxs-lookup"><span data-stu-id="dd77b-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="dd77b-126">Si el  _parámetro lpszFileName_ no está establecido, esta marca y STGM_DELETEONRELEASE deben establecerse.</span><span class="sxs-lookup"><span data-stu-id="dd77b-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="dd77b-127">Si STGM_CREATE se establece, también STGM_READWRITE debe establecerse la marca de STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="dd77b-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="dd77b-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="dd77b-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="dd77b-129">El archivo se eliminará cuando se libera el objeto **IStream.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="dd77b-130">Si el  _parámetro lpszFileName_ no está establecido, esta marca y STGM_CREATE deben establecerse.</span><span class="sxs-lookup"><span data-stu-id="dd77b-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="dd77b-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="dd77b-131">STGM_READ</span></span>
  
> <span data-ttu-id="dd77b-132">El archivo se va a crear o abrir con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd77b-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="dd77b-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="dd77b-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="dd77b-134">El archivo se va a crear o abrir con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dd77b-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="dd77b-135">Si no se establece esta marca, la STGM_CREATE no debe establecerse.</span><span class="sxs-lookup"><span data-stu-id="dd77b-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="dd77b-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="dd77b-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="dd77b-137">[in] Nombre de archivo, incluida la ruta de acceso y la extensión, del archivo con nombre Unicode para el que **OpenStreamOnFileW** inicializa el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="dd77b-138">Si se SOF_UNIQUEFILENAME marca,  _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="dd77b-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="dd77b-139">Si  _lpszFileName_ es NULL, **OpenStreamOnFileW** obtiene una ruta de acceso adecuada del sistema y se deben establecer las marcas STGM_CREATE y STGM_DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="dd77b-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="dd77b-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="dd77b-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="dd77b-141">[in] Prefijo del nombre de archivo Unicode en el que **OpenStreamOnFileW** inicializa el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="dd77b-142">Si se establece, el prefijo no debe contener más de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="dd77b-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="dd77b-143">Si  _lpszPrefix_ es NULL, se usa un prefijo de "SOF".</span><span class="sxs-lookup"><span data-stu-id="dd77b-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="dd77b-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="dd77b-144">_lppStream_</span></span>
  
> <span data-ttu-id="dd77b-145">[salida] Puntero a un puntero a un objeto que expone la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dd77b-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd77b-146">Return value</span></span>

<span data-ttu-id="dd77b-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd77b-147">S_OK</span></span>
  
> <span data-ttu-id="dd77b-148">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="dd77b-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="dd77b-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dd77b-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="dd77b-150">No se pudo tener acceso al archivo debido a que los permisos de usuario no son suficientes o porque no se pueden modificar los archivos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd77b-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="dd77b-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dd77b-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="dd77b-152">El archivo designado no existe.</span><span class="sxs-lookup"><span data-stu-id="dd77b-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd77b-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd77b-153">Remarks</span></span>

<span data-ttu-id="dd77b-154">La **función OpenStreamOnFileW** tiene dos usos importantes además de controlar un archivo con un nombre Unicode, que se distingue por la configuración de la marca SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="dd77b-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="dd77b-155">Cuando no se establece esta marca, **OpenStreamOnFileW** abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de un archivo adjunto mediante el método **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="dd77b-156">En este caso,  _el parámetro lpszFileName_ especifica la ruta de acceso y el nombre de archivo del archivo.</span><span class="sxs-lookup"><span data-stu-id="dd77b-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="dd77b-157">Cuando SOF_UNIQUEFILENAME se establece, **OpenStreamOnFileW** crea un archivo temporal para contener los datos de un **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="dd77b-158">Para este uso, el parámetro  _lpszFileName_ puede designar opcionalmente la ruta de acceso al directorio donde se va a crear el archivo y el parámetro  _lpszPrefix_ puede especificar opcionalmente un prefijo para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="dd77b-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="dd77b-159">Cuando la aplicación cliente de llamada o el proveedor de servicios termine con el objeto **IStream,** debe liberarla llamando al método OLE **IStream::Release.**</span><span class="sxs-lookup"><span data-stu-id="dd77b-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="dd77b-160">MAPI usa las funciones apuntadas por  _lpAllocateBuffer_ y  _lpFreeBuffer_ para la mayoría de la asignación y desasignación de memoria, en particular para asignar memoria para su uso por las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="dd77b-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dd77b-161">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="dd77b-161">Notes to callers</span></span>

<span data-ttu-id="dd77b-162">La SOF_UNIQUEFILENAME se usa para crear un archivo temporal con un nombre único para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="dd77b-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="dd77b-163">Si se establece esta marca, el parámetro  _lpszFileName_ especifica la ruta de acceso del archivo temporal y el parámetro  _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="dd77b-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="dd77b-164">El nombre de archivo construido es <prefix> HHHH. TMP, donde HHHH es un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="dd77b-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="dd77b-165">Si _lpszFileName_ es NULL, el archivo se creará en el directorio de archivos temporales que se devuelve de la función Windows **GetTempPath** o en el directorio actual si no se ha designado ningún directorio de archivos temporal.</span><span class="sxs-lookup"><span data-stu-id="dd77b-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="dd77b-166">Si no se establece la marca SOF_UNIQUEFILENAME, se omite  _lpszPrefix_ y  _lpszFileName_ debe contener la ruta de acceso completa y el nombre de archivo del archivo que se va a abrir o crear.</span><span class="sxs-lookup"><span data-stu-id="dd77b-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="dd77b-167">El archivo se abrirá o creará en función de las otras marcas establecidas en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="dd77b-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dd77b-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd77b-168">See also</span></span>



[<span data-ttu-id="dd77b-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="dd77b-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

